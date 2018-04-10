---
title: "Så här skapar du Fabrikskalendrar | Microsoft Docs"
description: "I en produktionsgruppkalender anger du de arbetsdagar och arbetstimmar, skift, helgdagar och frånvaro som avgör den tillgängliga bruttokapaciteten för produktionsgruppen (mätt i tidsenheter) utifrån de effektivitets- och kapacitetsvärden som har definierats för gruppen. Om du vill skapa och aktivera en produktionsgruppkalender måste du först utföra flera förberedande åtgärder."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a22dc01284fc0edca46d1f733f0bef83e61adbde
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-shop-calendars"></a><span data-ttu-id="afd49-104">Så här lägger du upp fabrikskalendrar</span><span class="sxs-lookup"><span data-stu-id="afd49-104">Set Up Shop Calendars</span></span>
<span data-ttu-id="afd49-105">I en produktionsgrupp- eller maskingruppkalender anger du de arbetsdagar/arbetstimmar, skift, helgdagar och frånvaro som avgör den tillgängliga bruttokapaciteten för produktionsgruppen (mätt i tidsenheter) utifrån de effektivitets- och kapacitetsvärden som har definierats för gruppen.</span><span class="sxs-lookup"><span data-stu-id="afd49-105">A work center or machine calendar specifies the working days and hours, shifts, holidays, and absences that determine the center’s gross available capacity, measured in time, according to its defined efficiency and capacity values.</span></span>

<span data-ttu-id="afd49-106">Om du vill beräkna en specifik produktionsgrupp- eller maskingruppkalender måste du först skapa en eller flera allmänna fabrikskalendrar.</span><span class="sxs-lookup"><span data-stu-id="afd49-106">As a foundation for calculating a specific work or machine center calendar, you must first set up one or more general shop calendars.</span></span> <span data-ttu-id="afd49-107">En fabrikskalender innehåller en standardarbetsvecka med start- och sluttider för varje arbetsdag samt en översikt över arbetsskiften.</span><span class="sxs-lookup"><span data-stu-id="afd49-107">A shop calendar defines a standard work week according to start and end times of each working day and the work shift relation.</span></span> <span data-ttu-id="afd49-108">Dessutom kan du i fabrikskalendern se de fasta helgdagarna under året.</span><span class="sxs-lookup"><span data-stu-id="afd49-108">In addition, the shop calendar defines the fixed holidays during a year.</span></span>  

<span data-ttu-id="afd49-109">Nedan beskrivs hur du ställer in produktionsgruppskalendrar.</span><span class="sxs-lookup"><span data-stu-id="afd49-109">The following describes how to set up work center calendars.</span></span> <span data-ttu-id="afd49-110">Momentet är liknande när du ställer in maksingruppkalender.</span><span class="sxs-lookup"><span data-stu-id="afd49-110">The steps are similar when setting up machine center calendars.</span></span>  

## <a name="to-create-work-shifts"></a><span data-ttu-id="afd49-111">Så här skapar du arbetsskift</span><span class="sxs-lookup"><span data-stu-id="afd49-111">To create work shifts</span></span>  
1.  <span data-ttu-id="afd49-112">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Arbetsskift** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="afd49-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Shifts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="afd49-113">På en tom rad anger du ett nummer i fältet **Kod** för att identifiera arbetsskiftet (till exempel **1**).</span><span class="sxs-lookup"><span data-stu-id="afd49-113">On a blank line, enter a number in the **Code** field to identify the work shift, for example, **1**.</span></span>  
3.  <span data-ttu-id="afd49-114">Beskriv arbetsskiftet i fältet **Beskrivning**, till exempel **1:a skift**.</span><span class="sxs-lookup"><span data-stu-id="afd49-114">Describe the work shift in the **Description** field, for example, **1st shift**.</span></span>  
4.  <span data-ttu-id="afd49-115">Fyll i raderna för ett andra eller tredje skift, om du vill.</span><span class="sxs-lookup"><span data-stu-id="afd49-115">Optionally, fill in lines for a second or third work shift.</span></span>  

<span data-ttu-id="afd49-116">Även om dina produktionsgrupper inte arbetar i olika skift måste du ange minst en arbetsskiftkod.</span><span class="sxs-lookup"><span data-stu-id="afd49-116">Even if your work centers do not work in different work shifts, enter at least one work shift code.</span></span>  

## <a name="to-set-up-a-shop-calendar"></a><span data-ttu-id="afd49-117">Så här skapar du en fabrikskalender</span><span class="sxs-lookup"><span data-stu-id="afd49-117">To set up a shop calendar</span></span>  
1.  <span data-ttu-id="afd49-118">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Arbetsskift** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="afd49-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Shop Calendars**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="afd49-119">På en tom rad anger du ett nummer i fältet **Kod** för att identifiera fabrikskalendern.</span><span class="sxs-lookup"><span data-stu-id="afd49-119">On a blank line, enter a number in the **Code** field to identify the shop calendar.</span></span>  
3.  <span data-ttu-id="afd49-120">Beskriv fabrikskalendern i fältet **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="afd49-120">Describe the shop calendar in the **Description** field.</span></span>  
4.  <span data-ttu-id="afd49-121">Välj åtgärden **arbetsdagar**.</span><span class="sxs-lookup"><span data-stu-id="afd49-121">Choose the **Working Days** action.</span></span>
5.  <span data-ttu-id="afd49-122">I fönstret **Fabrikskalender arbetsdagar** kan du definiera en fullständig arbetsvecka med start- och sluttider för varje dag.</span><span class="sxs-lookup"><span data-stu-id="afd49-122">In the **Shop Calendar Working Days** window, define a complete work week, with the start and end times for each day.</span></span>  

    <span data-ttu-id="afd49-123">I fältet **Arbetsskiftskod**, markera en av förskjutningarna som du definierade tidigare.</span><span class="sxs-lookup"><span data-stu-id="afd49-123">In the **Work Shift Code** field, select one of the shifts that you previously defined.</span></span> <span data-ttu-id="afd49-124">Lägg till en rad för varje arbetsdag, samt varje skift.</span><span class="sxs-lookup"><span data-stu-id="afd49-124">Add a line for every working day and every shift.</span></span> <span data-ttu-id="afd49-125">Som exempel:</span><span class="sxs-lookup"><span data-stu-id="afd49-125">For example:</span></span>  

    <span data-ttu-id="afd49-126">Måndag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="afd49-126">Monday  07:00 15:00 1</span></span>   
    <span data-ttu-id="afd49-127">Tisdag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="afd49-127">Tuesday 07:00 15:00 1</span></span>  

    <span data-ttu-id="afd49-128">Om du behöver en fabrikskalender med två arbetsskift måste du fylla i den på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="afd49-128">If you need a shop calendar with two work shifts, you must fill it in in this manner:</span></span>  

    <span data-ttu-id="afd49-129">Måndag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="afd49-129">Monday 07:00 15:00 1</span></span>   
    <span data-ttu-id="afd49-130">Måndag 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="afd49-130">Monday 15:00 23:00 2</span></span>  
    <span data-ttu-id="afd49-131">Tisdag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="afd49-131">Tuesday 07:00 15:00 1</span></span>  
    <span data-ttu-id="afd49-132">Tisdag 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="afd49-132">Tuesday 15:00 23:00 2</span></span>  

    <span data-ttu-id="afd49-133">De veckodagar som du inte definierar i fabrikskalendern, till exempel lördag och söndag, antas vara icke-arbetsdagar och får arbetskapaciteten noll i alla produktionsgruppkalendrar.</span><span class="sxs-lookup"><span data-stu-id="afd49-133">Any week days that you do not define in the shop calendar, such as Saturday and Sunday, are considered non-working days and will have zero available capacity in a work center calendar.</span></span>  

    <span data-ttu-id="afd49-134">När du har definierat alla arbetsdagar i veckan kan du stänga fönstret **Fabrikskalender arbetsdagar** och fortsätta med att ange helgdagar.</span><span class="sxs-lookup"><span data-stu-id="afd49-134">When all the working days of a week are defined, you can close the **Shop Calendar Working Days** window and proceed to enter holidays.</span></span>  

6.  <span data-ttu-id="afd49-135">I fönstret **fabrikskalender** markerar du fabrikskalendern, och väljer sedan åtgärden **helgdagar**.</span><span class="sxs-lookup"><span data-stu-id="afd49-135">In the **Shop Calendars** window, select the shop calendar, and then choose the **Holidays** action.</span></span>
7. <span data-ttu-id="afd49-136">I fönstret **Fabrikskalender semestrar** anger du helgdagar under året genom att ange startdatum och starttid, sluttid och en beskrivning av varje dag på enskilda rader.</span><span class="sxs-lookup"><span data-stu-id="afd49-136">In the **Shop Calendar Holidays** window, define the holidays of the year by entering the start date and time, the end time, and description of each holiday on individual lines.</span></span> <span data-ttu-id="afd49-137">Som exempel:</span><span class="sxs-lookup"><span data-stu-id="afd49-137">For example:</span></span>  

    <span data-ttu-id="afd49-138">04/07/14 0:00:00 23:59:00 Sommarsemester</span><span class="sxs-lookup"><span data-stu-id="afd49-138">04/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="afd49-139">05/07/14 0:00:00 23:59:00 Sommarsemester</span><span class="sxs-lookup"><span data-stu-id="afd49-139">05/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="afd49-140">06/07/14 0:00:00 23:59:00 Sommarsemester</span><span class="sxs-lookup"><span data-stu-id="afd49-140">06/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  

<span data-ttu-id="afd49-141">De angivna helgdagarna får värdet noll för tillgänglig kapacitet i alla produktionsgruppkalendrar.</span><span class="sxs-lookup"><span data-stu-id="afd49-141">The defined holidays will have zero available capacity in a work center calendar.</span></span>  

<span data-ttu-id="afd49-142">Fabrikskalendern kan nu tilldelas en produktionsgrupp så att den produktionsgruppkalender som styr all verksamhetstidsplanering för produktionsgruppen kan beräknas.</span><span class="sxs-lookup"><span data-stu-id="afd49-142">The shop calendar can now be assigned to a work center to calculate the work shop calendar that will govern all operation scheduling at that work center.</span></span>  

## <a name="to-calculate-a-work-center-calendar"></a><span data-ttu-id="afd49-143">Så här beräknar du en produktionsgruppkalender</span><span class="sxs-lookup"><span data-stu-id="afd49-143">To calculate a work center calendar</span></span>  

1.  <span data-ttu-id="afd49-144">Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Arbetsskift** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="afd49-144">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Centers**, and then choose the related link.</span></span>
2. <span data-ttu-id="afd49-145">Öppna produktionsgruppen som du vill uppdatera.</span><span class="sxs-lookup"><span data-stu-id="afd49-145">Open the work center that you want to update.</span></span>  
3. <span data-ttu-id="afd49-146">I fältet **Fabrikskalenderkod** väljer du vilken fabrikskalender som ska användas som grund för en produktionsgruppkalender.</span><span class="sxs-lookup"><span data-stu-id="afd49-146">In the **Shop Calendar Code** field, select which shop calendar to use as the foundation for a work center calendar.</span></span>  
4. <span data-ttu-id="afd49-147">Välj åtgärden **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="afd49-147">Choose the **Calendar** action.</span></span>  
5. <span data-ttu-id="afd49-148">I fönstret **Prod.gruppkalender** väljer du åtgärden **Visa matris**.</span><span class="sxs-lookup"><span data-stu-id="afd49-148">In the **Work Center Calendar** window, choose the **Show Matrix** action.</span></span>  

    <span data-ttu-id="afd49-149">Till vänster i matrisfönstret visas befintliga produktionsgrupper.</span><span class="sxs-lookup"><span data-stu-id="afd49-149">The left side of the matrix window lists the work centers that are set up.</span></span> <span data-ttu-id="afd49-150">Till höger visas en tidskalender med värden för tillgänglig kapacitet för varje arbetsdag i den angivna enheten, till exempel **480** minuter.</span><span class="sxs-lookup"><span data-stu-id="afd49-150">The right side shows a calendar displaying the available capacity values for each working day in the defined unit of measure, for example, **480** minutes.</span></span> <span data-ttu-id="afd49-151">Varje rad motsvarar kalendern för en produktionsgrupp.</span><span class="sxs-lookup"><span data-stu-id="afd49-151">Each line represents the calendar of one work center.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="afd49-152">Du kan också ange att du vill visa kapacitetsvärdena per vecka eller månad genom att ändra alternativen i fältet **Visa efter** i fönstret **Prod.gruppkalender**.</span><span class="sxs-lookup"><span data-stu-id="afd49-152">You can also select to view the capacity values for each week or month by changing the selection in the **View By** field in the **Work Center Calendar** window.</span></span>  

    <span data-ttu-id="afd49-153">Innan du kan visa den nya fabrikskalendern som en rad på den markerade produktionsgruppen måste den först beräknas.</span><span class="sxs-lookup"><span data-stu-id="afd49-153">To reflect the new shop calendar as a line on the selected work center, it must first be calculated.</span></span>  

6.  <span data-ttu-id="afd49-154">Välj åtgärden **Beräkna**.</span><span class="sxs-lookup"><span data-stu-id="afd49-154">Choose the **Calculate** action.</span></span>  
7.  <span data-ttu-id="afd49-155">På snabbfliken **Produktionsgrupp** kan du ange ett filter så att beräkningen bara utförs för en produktionsgrupp.</span><span class="sxs-lookup"><span data-stu-id="afd49-155">On the **Work Center** FastTab, you can set a filter to only calculate for one work center.</span></span> <span data-ttu-id="afd49-156">Om du inte anger något filter beräknas alla befintliga produktionsgruppkalendrar.</span><span class="sxs-lookup"><span data-stu-id="afd49-156">If you do not set a filter, all existing work center calendars will be calculated.</span></span>  
8.  <span data-ttu-id="afd49-157">Ange start- och sluttider för kalenderperioden som ska beräknas, till exempel ett år mellan 040101 och 041232.</span><span class="sxs-lookup"><span data-stu-id="afd49-157">Define the starting and ending dates of the calendar period that should be calculated, for example, one year from 01/01/14 to 31/12/14.</span></span>
9. <span data-ttu-id="afd49-158">Klicka på **OK** för att beräkna kapacitet.</span><span class="sxs-lookup"><span data-stu-id="afd49-158">Choose the **OK** button to calculate capacity.</span></span>  

<span data-ttu-id="afd49-159">Kalendertransaktioner skapas (eller uppdateras), och du ser den tillgängliga kapaciteten per period enligt följande tre uppsättningar standarduppgifter:</span><span class="sxs-lookup"><span data-stu-id="afd49-159">Calendar entries are now created or updated displaying the available capacity for each period according to the following three sets of master data:</span></span>  

- <span data-ttu-id="afd49-160">De arbetsdagar och skift som har angetts i den tilldelade fabrikskalendern.</span><span class="sxs-lookup"><span data-stu-id="afd49-160">The working days and shift defined in the assigned shop calendar.</span></span>  
- <span data-ttu-id="afd49-161">Värdet i fältet **Kapacitet** på produktionsgruppkortet.</span><span class="sxs-lookup"><span data-stu-id="afd49-161">The value in the **Capacity** field on the work center card.</span></span>  
- <span data-ttu-id="afd49-162">Värdet i fältet **Effektivitet** på produktionsgruppkortet.</span><span class="sxs-lookup"><span data-stu-id="afd49-162">The value in the **Efficiency** field on the work center card.</span></span>  

<span data-ttu-id="afd49-163">Den beräknade produktionsgruppkalendern definierar nu när, och hur mycket, som är tillgänglig kapacitet för produktionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="afd49-163">The calculated work center calendar will now define when and how much capacity is available at this work center.</span></span> <span data-ttu-id="afd49-164">Detta styr detaljerat planeringen av operationer som utförs i produktionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="afd49-164">This controls the detailed scheduling of operations performed at the work center.</span></span>  

## <a name="to-record-work-center-absence"></a><span data-ttu-id="afd49-165">Så här registrerar du frånvaro i produktionsgrupper</span><span class="sxs-lookup"><span data-stu-id="afd49-165">To record work center absence</span></span>  
1.  <span data-ttu-id="afd49-166">I fönstret **Prod.gruppkalender** väljer du åtgärden **Visa matris**.</span><span class="sxs-lookup"><span data-stu-id="afd49-166">In the **Work Center Calendar** window, choose the **Show Matrix** action.</span></span>
2. <span data-ttu-id="afd49-167">I fönstret **Prod.gruppkalendermatris** markerar du den produktionsgrupp och den kalenderdag som frånvarotid ska registreras för och väljer åtgärden **Frånvaro**.</span><span class="sxs-lookup"><span data-stu-id="afd49-167">In the **Work Center Calendar Matrix** window, select the work center and calendar day when the absence time should be recorded, and then choose the **Absence** action.</span></span>  
3.  <span data-ttu-id="afd49-168">I fönstret **Frånvaro** anger du starttid, sluttid och beskrivning av frånvarotiden.</span><span class="sxs-lookup"><span data-stu-id="afd49-168">In the **Absence** window, define the starting time, ending time, and description of that day’s absence.</span></span> <span data-ttu-id="afd49-169">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="afd49-169">For example:</span></span>  

    <span data-ttu-id="afd49-170">010125 08:00 10:00 Underhåll</span><span class="sxs-lookup"><span data-stu-id="afd49-170">25/01/01 08:00 10:00 Maintenance</span></span>  

4.  <span data-ttu-id="afd49-171">Välj åtgärden **uppdatering** och stäng fönstret **frånvaro**.</span><span class="sxs-lookup"><span data-stu-id="afd49-171">Choose the **Update** action, and then close the **Absence** window.</span></span>  

<span data-ttu-id="afd49-172">Kapaciteten för den markerade dagen minskas med den registrerade frånvarotiden.</span><span class="sxs-lookup"><span data-stu-id="afd49-172">The capacity of the selected day has now decreased by the recorded absence time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="afd49-173">Se även</span><span class="sxs-lookup"><span data-stu-id="afd49-173">See Also</span></span>  
[<span data-ttu-id="afd49-174">Skapa baskalendrar</span><span class="sxs-lookup"><span data-stu-id="afd49-174">Set Up Base Calendars</span></span>](across-how-to-assign-base-calendars.md)  
[<span data-ttu-id="afd49-175">Ställa in produktionsgrupper och maskingrupper</span><span class="sxs-lookup"><span data-stu-id="afd49-175">Set Up Work Centers and Machine Centers</span></span>](production-how-to-set-up-work-and-machine-centers.md)  
[<span data-ttu-id="afd49-176">Ställa in Produktion</span><span class="sxs-lookup"><span data-stu-id="afd49-176">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="afd49-177">Produktion</span><span class="sxs-lookup"><span data-stu-id="afd49-177">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="afd49-178">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="afd49-178">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
