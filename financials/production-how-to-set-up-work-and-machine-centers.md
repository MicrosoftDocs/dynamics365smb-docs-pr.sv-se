---
title: "Så här ställer du in produktions- och maskingrupper | Microsoft Docs"
description: "På ett **Produktionsgrupp**-kort ordnar du fasta värden och behov för produktionsresursen. På så sätt kan du styra utdata från den produktion som utförs i produktionsgruppen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/19/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: c06f828b50d217404bcdd3caafeb8843b40faffc
ms.contentlocale: sv-se
ms.lasthandoff: 09/27/2017

---
# <a name="how-to-set-up-work-centers-and-machine-centers"></a><span data-ttu-id="901cd-103">Så här: ställa in produktionsgrupper och maskingrupper</span><span class="sxs-lookup"><span data-stu-id="901cd-103">How to: Set Up Work Centers and Machine Centers</span></span>
<span data-ttu-id="901cd-104">Programmet skiljer mellan tre typer av kapaciteter.</span><span class="sxs-lookup"><span data-stu-id="901cd-104">The program distinguishes between three types of capacities.</span></span> <span data-ttu-id="901cd-105">Dessa är ordnade i hierarkisk ordning.</span><span class="sxs-lookup"><span data-stu-id="901cd-105">These are arranged hierarchically.</span></span> <span data-ttu-id="901cd-106">Varje nivå innehåller underordnade nivåer.</span><span class="sxs-lookup"><span data-stu-id="901cd-106">Each level contains the subordinate levels.</span></span>  

<span data-ttu-id="901cd-107">Den översta nivån är produktionsavdelningen.</span><span class="sxs-lookup"><span data-stu-id="901cd-107">The top level is the work center group.</span></span> <span data-ttu-id="901cd-108">Till produktionsavdelningarna är produktionsgrupper kopplade.</span><span class="sxs-lookup"><span data-stu-id="901cd-108">Work centers are assigned to the work center groups.</span></span> <span data-ttu-id="901cd-109">Varje produktionsgrupp kan endast tillhöra en produktionsavdelning.</span><span class="sxs-lookup"><span data-stu-id="901cd-109">Every work center can only belong to one work center group.</span></span>

<span data-ttu-id="901cd-110">Olika maskingrupper kan kopplas till varje produktionsgrupp.</span><span class="sxs-lookup"><span data-stu-id="901cd-110">You can assign various machine centers to every work center.</span></span> <span data-ttu-id="901cd-111">En maskingrupp kan endast tillhöra en produktionsgrupp.</span><span class="sxs-lookup"><span data-stu-id="901cd-111">A machine center may only belong to one work center.</span></span>  

<span data-ttu-id="901cd-112">En produktionsgrupps planerade kapacitet består av motsvarande maskingrupps disposition och ytterligare planerad produktionsgruppsdisposition.</span><span class="sxs-lookup"><span data-stu-id="901cd-112">The planned capacity of a work center consists of the availability of the corresponding machine centers and the additional planned availability of the work center.</span></span> <span data-ttu-id="901cd-113">Den planerade dispositionen i produktionsavdelningen är alltså summan av alla motsvarande maskin- och produktionsgruppsdispositioner.</span><span class="sxs-lookup"><span data-stu-id="901cd-113">The planned availability of the work center group is, therefore, the sum of all corresponding availabilities of the machine centers and work centers.</span></span>  

<span data-ttu-id="901cd-114">Dispositionen lagras i kalendertransaktioner.</span><span class="sxs-lookup"><span data-stu-id="901cd-114">The availability is stored in calendar entries.</span></span> <span data-ttu-id="901cd-115">Innan du ställer in produktions- eller maskingrupper, måste du lägga upp fabrikskalendrar.</span><span class="sxs-lookup"><span data-stu-id="901cd-115">Before you set up work or machine centers, you must set up shop calendars.</span></span> <span data-ttu-id="901cd-116">För mer information, se [Så här skapar du Fabrikskalendrar](production-how-to-create-work-center-calendars.md).</span><span class="sxs-lookup"><span data-stu-id="901cd-116">For more information, see [How to: Create Shop Calendars](production-how-to-create-work-center-calendars.md).</span></span>  

## <a name="to-set-up-a-work-center"></a><span data-ttu-id="901cd-117">Så här skapar du produktionsgrupper:</span><span class="sxs-lookup"><span data-stu-id="901cd-117">To set up a work center</span></span>
<span data-ttu-id="901cd-118">Nedan beskrivs hur du ställer in produktionsgrupp</span><span class="sxs-lookup"><span data-stu-id="901cd-118">The following primarily describes how to set up a work center.</span></span> <span data-ttu-id="901cd-119">Stegen för att ställa in maskingruppkalender är liknande förutom snabbfliken **operationsföljdinställningar**.</span><span class="sxs-lookup"><span data-stu-id="901cd-119">The steps to set up a machine center calendar are similar except for the **Routing Setup** FastTab.</span></span>  

1.  <span data-ttu-id="901cd-120">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Arbetsskift** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="901cd-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="901cd-121">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="901cd-121">Choose the **New** action.</span></span>  
3. <span data-ttu-id="901cd-122">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="901cd-122">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="901cd-123">I fältet **Produktionsavdelning** väljer du den resursgrupp på högre nivå som produktionsgruppen är underordnad.</span><span class="sxs-lookup"><span data-stu-id="901cd-123">In the **Work Center Group** field, select the higher-level resource grouping that the work center is organized under, if relevant.</span></span> <span data-ttu-id="901cd-124">Välj åtgärden **Ny** i listrutan.</span><span class="sxs-lookup"><span data-stu-id="901cd-124">Choose the **New** action in the drop-down list.</span></span>  
5.  <span data-ttu-id="901cd-125">Välj fältet **Spärrad** om du vill förhindra att produktionsgruppen används i någon behandling.</span><span class="sxs-lookup"><span data-stu-id="901cd-125">Select the **Blocked** field if you want to prevent the work center from being used in any processing.</span></span> <span data-ttu-id="901cd-126">Detta innebär att produktionen inte kan bokföras för en artikel som produceras i produktionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="901cd-126">This means that output cannot be posted for an item that is produced at the work center.</span></span> <span data-ttu-id="901cd-127">För mer information, se [Så här bokför du produktionsutflödet](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="901cd-127">For more information, see [How to: Post Production Output](production-how-to-post-output-quantity.md).</span></span>
6.  <span data-ttu-id="901cd-128">I fältet **Inköpspris** anger du kostnaden för att producera en enhet i denna produktionsgrupp, exklusive alla andra kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="901cd-128">In the **Direct Unit Cost** field, enter the cost of producing one unit of measure at this work center, excluding any other cost elements.</span></span> <span data-ttu-id="901cd-129">Denna kostnad kallas ofta för *direkt arbetskostnad*.</span><span class="sxs-lookup"><span data-stu-id="901cd-129">This cost is often referred to as the *direct labor rate*.</span></span>  
7.  <span data-ttu-id="901cd-130">I fältet **Indirekt kostnad %** anger du de allmänna operationskostnaderna för att använda produktionsgruppen som en procentandel av inköpspriset.</span><span class="sxs-lookup"><span data-stu-id="901cd-130">In the **Indirect Cost %** field, enter the general operation costs of using the work center as a percentage of the direct unit cost.</span></span> <span data-ttu-id="901cd-131">Denna procentandel läggs till inköpspriset vid beräkningen av styckkostnaden.</span><span class="sxs-lookup"><span data-stu-id="901cd-131">This percentage amount is added to the direct cost in the calculation of the unit cost.</span></span>  
8.  <span data-ttu-id="901cd-132">I fältet **Omkostnad** anger du icke-operationella kostnader för produktionsgruppen, till exempel underhållsutgifter, som ett absolut belopp.</span><span class="sxs-lookup"><span data-stu-id="901cd-132">In the **Overhead Rate** field, enter any non-operational costs, for example maintenance expenses, of the work center as an absolute amount.</span></span>  

    <span data-ttu-id="901cd-133">I fältet **Styckkostnad** visas den beräknade styckkostnaden för att producera en enhet i denna produktionsgrupp, inklusive alla kostnadselement.</span><span class="sxs-lookup"><span data-stu-id="901cd-133">The **Unit Cost** field contains the calculated unit cost of producing one unit of measure at this work center, including all cost elements, as follows:</span></span>  

    <span data-ttu-id="901cd-134">Styckkostnad = Inköpspris + (Inköpspris x Indirekt kostnad %) + Omkostnad.</span><span class="sxs-lookup"><span data-stu-id="901cd-134">Unit Cost = Direct Unit Cost + (Direct Unit Cost x Indirect Cost %) + Overhead Rate.</span></span>  

9.  <span data-ttu-id="901cd-135">I fältet **Styckkost. beräkningstyp** anger du om beräkningen ovan ska bygga på mängden tid som använts: **Tid** eller antalet enheter som har producerats: **Enheter**.</span><span class="sxs-lookup"><span data-stu-id="901cd-135">In the **Unit Cost Calculation** field, define whether the above calculation should be based on the amount of time used:  **Time**, or on the number of produced units:  **Units**.</span></span>  
10.  <span data-ttu-id="901cd-136">Markera fältet **Specifik styckkostnad** om du vill definiera styckkostnaden för produktionsgruppen på den operationsföljdrad där den används.</span><span class="sxs-lookup"><span data-stu-id="901cd-136">Select the **Specific Unit Cost** field if you want to define the work center’s unit cost on the routing line where it is being used.</span></span> <span data-ttu-id="901cd-137">Detta kan vara användbart för operationer där kapacitetskostnaden skiljer sig markant från vad som är normalt för produktionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="901cd-137">This may be relevant for operations with dramatically different capacity costs than what would normally be processed at that work center.</span></span>  
11.  <span data-ttu-id="901cd-138">I fältet **Bokföringsmetod** anger du om bokföring av utflöde i produktionsgruppen ska beräknas och bokföras manuellt eller om det ska ske automatiskt med någon av följande metoder.</span><span class="sxs-lookup"><span data-stu-id="901cd-138">In the **Flushing Method** field, select whether output posting at this work center should be calculated and posted manually or automatically, using either of the following methods.</span></span>  

    |<span data-ttu-id="901cd-139">Alternativ</span><span class="sxs-lookup"><span data-stu-id="901cd-139">Option</span></span>|<span data-ttu-id="901cd-140">Description</span><span class="sxs-lookup"><span data-stu-id="901cd-140">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="901cd-141">**Manuell**</span><span class="sxs-lookup"><span data-stu-id="901cd-141">**Manual**</span></span>|<span data-ttu-id="901cd-142">Förbrukning bokförs manuellt i utflödesjournalen eller produktionsjournal.</span><span class="sxs-lookup"><span data-stu-id="901cd-142">Concumption is posted manually in the output journal or production journal.</span></span>|
    |<span data-ttu-id="901cd-143">**Framåt**</span><span class="sxs-lookup"><span data-stu-id="901cd-143">**Forward**</span></span>|<span data-ttu-id="901cd-144">Förbrukning beräkna och bokförs automatiskt när produktionsordern släpps.</span><span class="sxs-lookup"><span data-stu-id="901cd-144">Consumption is calculated and posted automatically when the production order is released.</span></span>|  
    |<span data-ttu-id="901cd-145">**Bakåt**</span><span class="sxs-lookup"><span data-stu-id="901cd-145">**Backward**</span></span>|<span data-ttu-id="901cd-146">Förbrukning beräkna och bokförs automatiskt när produktionsordern är färdig.</span><span class="sxs-lookup"><span data-stu-id="901cd-146">Consumption is calculated and posted automatically when the production order is finished.</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="901cd-147">Om det behövs kan bokföringsmetoden som markeras här och på **artikelkortet** åsidosättas för enskilda operationer genom att inställningen för en operationsföljdrad ändras.</span><span class="sxs-lookup"><span data-stu-id="901cd-147">If necessary, the flushing method selected here and on the **Item** card, can be overridden for individual operations by changing the setting on routing lines.</span></span>

12.  <span data-ttu-id="901cd-148">I fältet **Enhetskod** anger du den tidsenhet som ska användas för beräkning av kostnad och kapacitetsplanering för produktionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="901cd-148">In the **Unit of Measure Code** field, enter the time unit in which this work center’s cost calculation and capacity planning are made.</span></span>
    <span data-ttu-id="901cd-149">För att kunna övervaka kapacitetsförbrukningen kontinuerligt måste du först ange en mätmetod.</span><span class="sxs-lookup"><span data-stu-id="901cd-149">In order to be able to constantly monitor consumption, you must first set up a method of measure.</span></span> <span data-ttu-id="901cd-150">Enheterna som du anger är grundläggande enheter.</span><span class="sxs-lookup"><span data-stu-id="901cd-150">The units you enter are basic units.</span></span> <span data-ttu-id="901cd-151">Exempelvis mäts bearbetningstiden i timmar och minuter.</span><span class="sxs-lookup"><span data-stu-id="901cd-151">For example, the processing time is measured in hours and minutes.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="901cd-152"> Om du väljer att använda Dagar är det vktigt att komma ihåg att 1 dag = 24 timmar - inte 8 (arbetstimmar).</span><span class="sxs-lookup"><span data-stu-id="901cd-152">If you select to use Days then remember that 1 day = 24 hours - and not 8 (working hours).</span></span>

13.  <span data-ttu-id="901cd-153">I fältet **Kapacitet** anger du om fler än en person eller maskin arbetar samtidigt i produktionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="901cd-153">In the **Capacity** field, define whether the work center has more than one machine or person working at the same time.</span></span> <span data-ttu-id="901cd-154">Om din **Produktnamn**-installation inte innehåller modulen Maskingrupp måste värdet i det är fältet vara **1**).</span><span class="sxs-lookup"><span data-stu-id="901cd-154">If your **Product Name** installation does not include the Machine Center functionality, then the value in this field must be **1**).</span></span>  
14.  <span data-ttu-id="901cd-155">I fältet **Effektivitet** anger du den procentandel av förväntade standardutdata som faktiskt uppnås av produktionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="901cd-155">In the **Efficiency** field, enter the percentage of the expected standard output that this work center actually outputs.</span></span> <span data-ttu-id="901cd-156">Genom att ange **100** kan du ange att produktionsgruppens faktiska utdata är samma som standardutdata.</span><span class="sxs-lookup"><span data-stu-id="901cd-156">If you enter **100**, it means that the work center has an actual output that is the same as the standard output.</span></span>  
15. <span data-ttu-id="901cd-157">Markera kryssrutan **Konsoliderad kalender** om du också använder maskingrupper.</span><span class="sxs-lookup"><span data-stu-id="901cd-157">Select the **Consolidated Calendar** check box if you are also using machine centers.</span></span> <span data-ttu-id="901cd-158">På så sätt uppsummeras kalendertransaktioner maskingruppkalender.</span><span class="sxs-lookup"><span data-stu-id="901cd-158">This ensures that calendar entries are rolled up from machine center calendars.</span></span>  
16.  <span data-ttu-id="901cd-159">I fältet **Fabrikskalenderkod** väljer du en fabrikskalender.</span><span class="sxs-lookup"><span data-stu-id="901cd-159">In the **Shop Calendar Code** field, select a shop calendar.</span></span> <span data-ttu-id="901cd-160">För mer information, se [Så här skapar du Fabrikskalendrar](production-how-to-create-work-center-calendars.md).</span><span class="sxs-lookup"><span data-stu-id="901cd-160">For more information, see [How to: Create Shop Calendars](production-how-to-create-work-center-calendars.md).</span></span>  
17.  <span data-ttu-id="901cd-161">I fältet **Kötid** anger du ett tidsintervall som måste gå innan tilldelat arbete kan påbörjas i produktionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="901cd-161">In the **Queue Time** field, specify a fixed time span that must pass before assigned work can begin at this work center.</span></span> <span data-ttu-id="901cd-162">Observera att värdet för Kötid läggs till utöver andra icke-produktiva tidselement som till exempel Väntetid och Transporttid, som du kan ange på operationsföljdrader som använder produktionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="901cd-162">Note that queue time is added to other non-productive time elements such as wait time and move time that you may define on routing lines using this work center.</span></span>  

## <a name="example---different-machine-centers-assigned-to-a-work-center"></a><span data-ttu-id="901cd-163">Exempel – Olika maskingrupper kan kopplas till en produktionsgrupp</span><span class="sxs-lookup"><span data-stu-id="901cd-163">Example - Different Machine Centers Assigned to a Work Center</span></span>
<span data-ttu-id="901cd-164">Det är viktigt att planera vad som ska utgöra den totala kapaciteten när maskin- och produktionsgrupper skapas.</span><span class="sxs-lookup"><span data-stu-id="901cd-164">It is important to plan which capacities are to make up the total capacity when setting up the machine centers and work centers.</span></span>

<span data-ttu-id="901cd-165">Om olika maskingrupper (till exempel 210 Packbord, 310 Målningshytt...) kopplats till en produktionsgrupp är det viktigt att beakta varje maskingrupps kapacitet eftersom ett fel i en enda maskingrupp kan avbryta hela processen.</span><span class="sxs-lookup"><span data-stu-id="901cd-165">If different machine centers (such as 210 Packing table 1, 310 Painting Cabin ...) are assigned to a work center, the consideration of the single capacities of the machine centers is significant because failure of one machine center can interrupt the entire process.</span></span> <span data-ttu-id="901cd-166">Maskingrupperna kan anges enligt kapacitet men kan inte inkluderas i planeringen.</span><span class="sxs-lookup"><span data-stu-id="901cd-166">The machine groups can be entered according to their capacity but may not be included in the planning.</span></span> <span data-ttu-id="901cd-167">Om fältet **Konsoliderad kalender** inaktiveras kopplas endast produktionsgruppens men inte maskingruppens kapacitet till planeringen.</span><span class="sxs-lookup"><span data-stu-id="901cd-167">By deactivating the **Consolidated Calendar** field only the capacity of the work center but not the machine center is assigned in the planning.</span></span>

<span data-ttu-id="901cd-168">Om däremot identiska maskingrupper (till exempel 210 Packbord 1 och 220 Packbord 2) kombineras i en produktionsgrupp, beaktas produktionsgruppen som summan av de kopplade maskingrupperna.</span><span class="sxs-lookup"><span data-stu-id="901cd-168">If, however, identical machine centers (such as 210 Packing table 1 and 220 Packing table 2) are combined in a work center, the consideration of the work center as a sum of the assigned machine centers is of interest.</span></span> <span data-ttu-id="901cd-169">Därför visas produktionsgruppen i detta fall med nollkapacitet.</span><span class="sxs-lookup"><span data-stu-id="901cd-169">Therefore, the work center would be listed with zero capacity.</span></span> <span data-ttu-id="901cd-170">Om fältet **Konsoliderad kalender** aktiveras så kopplas den gemensamma kapaciteten till produktionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="901cd-170">By activating the **Consolidated Calendar** field, the common capacity is assigned to the work center.</span></span>

<span data-ttu-id="901cd-171">Om produktionsgruppernas kapacitet inte ska läggas till i den totala kapaciteten anger du effektivitet = 0.</span><span class="sxs-lookup"><span data-stu-id="901cd-171">If capacities of work centers are to make no contribution to the total capacity, you can achieve this with efficiency = 0.</span></span>

## <a name="to-set-up-a-capacity-constrained-machine-or-work-center"></a><span data-ttu-id="901cd-172">Om du vill ställa in en kapacitetsbegränsad maskin- eller produktionsgrupp</span><span class="sxs-lookup"><span data-stu-id="901cd-172">To set up a capacity constrained machine or work center</span></span>
<span data-ttu-id="901cd-173">Du måste skapa produktionsresurser som du anser är kritiska och markera dem för att acceptera en bestämd beläggning i stället för den obestämda beläggning som är standard och som andra produktionsresurser accepterar.</span><span class="sxs-lookup"><span data-stu-id="901cd-173">You must set up production resources that you regard as critical and mark them to accept a finite load instead of the default infinite load that other production resources accept.</span></span> <span data-ttu-id="901cd-174">Ett kapacitetsbegränsad resurs kan vara en produktions- eller maskingrupp som du har identifierat som en flaskhals och för vilken du vill skapa en begränsad (bestämd) beläggning.</span><span class="sxs-lookup"><span data-stu-id="901cd-174">A capacity-constrained resource can be a work center or machine center that you have identified as a bottleneck and would like to establish a limited, finite load for.</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="901cd-175"> har inte stöd för detaljerad fabrikskontroll.</span><span class="sxs-lookup"><span data-stu-id="901cd-175"> does not support detailed shop floor control.</span></span> <span data-ttu-id="901cd-176">Den planerar för ett möjligt utnyttjande av resurser genom att ange grovt schema, men det skapar och underhåller inte automatiskt detaljerade scheman som baseras på prioriteter eller optimeringsregler.</span><span class="sxs-lookup"><span data-stu-id="901cd-176">It plans for a feasible utilization of resources by providing a rough-cut schedule, but it does not automatically create and maintain detailed schedules based on priorities or optimization rules.</span></span>

<span data-ttu-id="901cd-177">I fönstret **kapacitetsbegränsade resurser** kan du göra inställningar som undviker överbelastning av specifika resurser och säkerställa att ingen kapacitet blir ej fördelad om den kan öka produktionstiden för en produktionsorder.</span><span class="sxs-lookup"><span data-stu-id="901cd-177">In the **Capacity-Constrained Resources** window, you can make setup that avoids overload of specific resources and ensure that no capacity is left unallocated if it could increase the turn-around time of a production order.</span></span> <span data-ttu-id="901cd-178">I fältet **Dämpare (% totalkapacitet)** kan du lägga till dämpartiden för resurser för att minimera åtgärdsdelning.</span><span class="sxs-lookup"><span data-stu-id="901cd-178">In the **Dampener (% of Total Capacity)** field, you can add dampener time to resources to minimize operation splitting.</span></span> <span data-ttu-id="901cd-179">Det gör att systemet kan schemalägga laddning till den sista möjliga dagen genom att överskrida den kritiska beläggningsprocenten något om det kan minska antalet operationer som delas.</span><span class="sxs-lookup"><span data-stu-id="901cd-179">This enables the system to schedule load on the last possible day by exceeding the critical load percent slightly if this can reduce the number of operations that are split.</span></span>

<span data-ttu-id="901cd-180">När du ska planera med kapacitetsbegränsade resurser ser systemet till att ingen resurs beläggs över sin definierade kapacitet (kritisk beläggning).</span><span class="sxs-lookup"><span data-stu-id="901cd-180">When planning with capacity-constrained resources, the system ensures that no resource is loaded above its defined capacity (critical load).</span></span> <span data-ttu-id="901cd-181">Det ske genom att tilldela varje operation till den närmaste tillgängliga tidsluckan.</span><span class="sxs-lookup"><span data-stu-id="901cd-181">This is done by assigning each operation to the nearest available time slot.</span></span> <span data-ttu-id="901cd-182">Om tidsluckan inte är tillräckligt stor för att slutföra hela åtgärden kommer åtgärden att uppdelas i två eller flera delar som placeras i de närmaste tidsluckorna.</span><span class="sxs-lookup"><span data-stu-id="901cd-182">If the time slot is not big enough to complete the entire operation, then the operation will be split into two or more parts placed in the nearest available time slots.</span></span>

1. <span data-ttu-id="901cd-183">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Kap.begränsning för resurs** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="901cd-183">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Capacity Constrined Resources**, and then choose the related link.</span></span>
2. <span data-ttu-id="901cd-184">Välj åtgärden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="901cd-184">Choose the **New** action.</span></span>
3. <span data-ttu-id="901cd-185">Fyll i fälten om det behövs.</span><span class="sxs-lookup"><span data-stu-id="901cd-185">Fill in the fields as necessary.</span></span>

> [!NOTE]
> <span data-ttu-id="901cd-186">Operationer på produktions- eller maskingrupper, som definierar begränsade resurser ska alltid planeras i nummerserie.</span><span class="sxs-lookup"><span data-stu-id="901cd-186">Operations on work centers or machine centers that are set up as constrained resources will always be planned serially.</span></span> <span data-ttu-id="901cd-187">Det innebär att även om en begränsad resurs har flera kapaciteter, ska operationer som utförts av de kapaciteterna bara planeras i sekvens inte i parallell, vilket är fallet om maskingruppen inte har lagts upp som en begränsad resurs.</span><span class="sxs-lookup"><span data-stu-id="901cd-187">This means that if a constrained resource has multiple capacities, then those capacities can only be planned in sequence, not in parallel as they would be if the work or machine center was not set up as a constrained resource.</span></span> <span data-ttu-id="901cd-188">I en begränsad resurs är fältet Kapacitet för produktionsgruppen eller maskingruppen större än 1.</span><span class="sxs-lookup"><span data-stu-id="901cd-188">In a constrained resource, the Capacity field on the work center or machine center is greater than 1.</span></span>

> <span data-ttu-id="901cd-189">I händelse av åtgärdsdelning tilldelas inställningstiden bara en gång, eftersom det antas att vissa manuella justeringen sker för att optimera schemat.</span><span class="sxs-lookup"><span data-stu-id="901cd-189">In case of operation splitting, the setup time is only assigned once because it is assumed that some manual adjustment is done to optimize the schedule.</span></span>

## <a name="see-also"></a><span data-ttu-id="901cd-190">Se även</span><span class="sxs-lookup"><span data-stu-id="901cd-190">See Also</span></span>  
[<span data-ttu-id="901cd-191">Så här skapar du fabrikskalendrar</span><span class="sxs-lookup"><span data-stu-id="901cd-191">How to: Create Shop Calendars</span></span>](production-how-to-create-work-center-calendars.md)  
[<span data-ttu-id="901cd-192">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="901cd-192">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="901cd-193">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="901cd-193">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="901cd-194">[Planerad](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="901cd-194">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="901cd-195">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="901cd-195">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="901cd-196">Inköp</span><span class="sxs-lookup"><span data-stu-id="901cd-196">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="901cd-197">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="901cd-197">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
