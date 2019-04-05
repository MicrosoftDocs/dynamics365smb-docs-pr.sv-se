---
title: Bokföringsdatum för värdetransaktioner
description: Lär dig hur batch-jobbet Justera Kostnad - Artikeltransaktioner används för att identifiera och tilldela ett bokföringsdatum till de värdetransaktioner som batchjobbet håller på att skapa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: edupont
ms.openlocfilehash: 9d0a5ab6bebdc9723fe8e3621fdda3cb16d5e6e1
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807069"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a><span data-ttu-id="da93f-103">Designinformation: Bokföringsdatumet för justeringsvärdetransaktionen</span><span class="sxs-lookup"><span data-stu-id="da93f-103">Design Details: Posting Date on Adjustment Value Entry</span></span>
<span data-ttu-id="da93f-104">Den här artikeln innehåller riktlinjer för kostnadsberäkningsfunktioner för lager [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="da93f-104">This article provides guidance for users of the Inventory Costing functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="da93f-105">Den specifika artikeln vägleder dig i hur batchjobbet **Justera kostnad - Artikeltransaktioner** identifierar och tilldelar ett bokföringsdatum till de värdeposter som batchjobbet håller på att skapa.</span><span class="sxs-lookup"><span data-stu-id="da93f-105">The specific article is providing guidance in how the **Adjust Cost - Item Entries** batch job identifies and assigns a posting date to the value entries that the batch job is about to create.</span></span>  

<span data-ttu-id="da93f-106">Först granskas processens koncept, hur batch-jobbet identifierar och tilldelar bokföringsdatum till värdetransaktionen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="da93f-106">First the concept of the process is reviewed, how the batch job identifies and assigns the Posting Date to the Value Entry to be created.</span></span> <span data-ttu-id="da93f-107">Därefter delas vissa situationer som vi i supportteamet stöter på då, och slutligen kommer en sammanfattning av de begrepp som använd s i version 3.0.</span><span class="sxs-lookup"><span data-stu-id="da93f-107">Thereafter there are some scenarios shared that we in the support team come across from time to time and finally there is a summary of the concepts used from version 3.0.</span></span>  

## <a name="the-concept"></a><span data-ttu-id="da93f-108">Konceptet</span><span class="sxs-lookup"><span data-stu-id="da93f-108">The Concept</span></span>  
<span data-ttu-id="da93f-109">Från och med version 5.0 tilldelar batchjobbet **Justera kost.-artikeltrans** ett bokföringsdatum för den värdetransaktion den håller på att skapa genom följande steg:</span><span class="sxs-lookup"><span data-stu-id="da93f-109">From version 5.0, the **Adjust Cost – Item Entries** batch job assigns a posting date to the value entry it is about to create in the following steps:</span></span>  

1.  <span data-ttu-id="da93f-110">Bokföringsdatum för den transaktion som skapas är från början samma datum som för den transaktion den justerar.</span><span class="sxs-lookup"><span data-stu-id="da93f-110">Initially the Posting Date of the entry to be created is the same date as the entry it adjusts.</span></span>  

2.  <span data-ttu-id="da93f-111">Bokföringsdatum verifieras mot lagerperioder och/eller redovisningsinställningar.</span><span class="sxs-lookup"><span data-stu-id="da93f-111">The Posting Date is validated against Inventory Periods and/or General Ledger Setup.</span></span>  

3.  <span data-ttu-id="da93f-112">Fördelningen av bokföringsdatum: Om det ursprungliga bokföringsdatumet inte ligger inom tillåtet intervall, tilldelar batchjobbet ett tillåtet bokföringsdatum från antingen Redovisningsinställningar eller Lagerperiod.</span><span class="sxs-lookup"><span data-stu-id="da93f-112">Assignment of Posting Date; If the initial Posting Date is not within allowed posting date range the batch job will assign an allowed Posting Date from either General Ledger Setup or Inventory Period.</span></span> <span data-ttu-id="da93f-113">Om såväl lagerperioder som tillåtna bokföringsdatum i Redovisningsinställningar har angetts, kommer det senare av de två att tilldelas justeringsvärdetransaktionen.</span><span class="sxs-lookup"><span data-stu-id="da93f-113">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will be assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="da93f-114">Vi ska nu granska denna process i praktiken.</span><span class="sxs-lookup"><span data-stu-id="da93f-114">Let’s review this process more in practice.</span></span> <span data-ttu-id="da93f-115">Anta att vi har en försäljningspost för en artikeltransaktion.</span><span class="sxs-lookup"><span data-stu-id="da93f-115">Assume we have an Item Ledger Entry of Sale.</span></span> <span data-ttu-id="da93f-116">Artikeln skeppades iväg den 5 september 2013 och fakturerades dagen efter.</span><span class="sxs-lookup"><span data-stu-id="da93f-116">The item was shipped on September 5th, 2013 and it was invoiced the day after.</span></span>  

<span data-ttu-id="da93f-117">![Status för artikeltransaktioner i scenariot](media/helene/TechArticleAdjustcost1.png "Status för artikeltransaktioner i scenariot")</span><span class="sxs-lookup"><span data-stu-id="da93f-117">![State of item ledger entries in the scenario](media/helene/TechArticleAdjustcost1.png "State of item ledger entries in the scenario")</span></span>  

<span data-ttu-id="da93f-118">Nedan representerar den första värdetransaktionen (379) själva leveransen och bär samma bokföringsdatum som den överordnade artikeltransaktionen.</span><span class="sxs-lookup"><span data-stu-id="da93f-118">Below, the first Value Entry (379) represents the shipment and carry the same Posting Date as the parent Item ledger Entry.</span></span>  

<span data-ttu-id="da93f-119">Den andra värdetransaktionen (381) motsvarar fakturan.</span><span class="sxs-lookup"><span data-stu-id="da93f-119">The second Value Entry (381) represents the invoice.</span></span>  

 <span data-ttu-id="da93f-120">Den tredje värdetransaktionen (391) är en justering av värdetransaktionen för fakturering (381)</span><span class="sxs-lookup"><span data-stu-id="da93f-120">The third Value Entry (391) is an Adjustment of the invoicing Value Entry (381)</span></span>  

 <span data-ttu-id="da93f-121">![Status för värdetransaktioner i scenariot](media/helene/TechArticleAdjustcost2.png "Status för värdetransaktioner i scenariot")</span><span class="sxs-lookup"><span data-stu-id="da93f-121">![State of value entries in the scenario](media/helene/TechArticleAdjustcost2.png "State of value entries in the scenario")</span></span>  

 <span data-ttu-id="da93f-122">Steg 1: Justeringsvärdetransaktionen som ska skapas tilldelas samma bokföringsdatum som den transaktion den justerar, vilket illustreras ovan genom värdetransaktion 391.</span><span class="sxs-lookup"><span data-stu-id="da93f-122">Step 1: Adjustment Value Entry to be created is assigned same Posting Date as the entry it adjusts, illustrated above by Value entry 391.</span></span>  

 <span data-ttu-id="da93f-123">Steg 2: Validering av ursprungligen tilldelat bokföringsdatum.</span><span class="sxs-lookup"><span data-stu-id="da93f-123">Step 2: Validation of initial assigned Posting Date.</span></span>  

<span data-ttu-id="da93f-124">Batchjobbet **Justera kost.-artikeltrans** avgör om justeringsvärdetransaktionens inledande bokföringsdatum ligger inom tillåtet spann för bokföringsdatum baserat på lagerperioder och/eller redovisningsinställningar.</span><span class="sxs-lookup"><span data-stu-id="da93f-124">The **Adjust Cost – Item Entries** batch job determines if the initial Posting Date of the Adjustment Value Entry is within allowed posting date range based upon Inventory Periods and/or General Ledger Setup.</span></span>  

 <span data-ttu-id="da93f-125">Vi ska nu granska ovannämnda försäljning genom att lägga till inställningen av tillåtna datumintervall för bokföring.</span><span class="sxs-lookup"><span data-stu-id="da93f-125">Let’s review the above mentioned Sale by adding setup of allowed posting date ranges.</span></span>  

 <span data-ttu-id="da93f-126">Lagerperioder:</span><span class="sxs-lookup"><span data-stu-id="da93f-126">Inventory Periods:</span></span>  

<span data-ttu-id="da93f-127">![Lagerperioden i scenariot](media/helene/TechArticleAdjustcost3.png "Lagerperioden i scenariot")</span><span class="sxs-lookup"><span data-stu-id="da93f-127">![Inventory periods in the scenario](media/helene/TechArticleAdjustcost3.png "Inventory periods in the scenario")</span></span>

 <span data-ttu-id="da93f-128">Första tillåtna bokföringsdatum är den första dagen i den första öppna perioden.</span><span class="sxs-lookup"><span data-stu-id="da93f-128">First allowed posting date is the first day in the first open period.</span></span> <span data-ttu-id="da93f-129">1 september 2013.</span><span class="sxs-lookup"><span data-stu-id="da93f-129">September 1st, 2013.</span></span>  

 <span data-ttu-id="da93f-130">Redovisningsinställningar:</span><span class="sxs-lookup"><span data-stu-id="da93f-130">General Ledger Setup:</span></span>  

<span data-ttu-id="da93f-131">![Inställningarna för Redovisning i scenariot](media/helene/TechArticleAdjustcost4.png "Inställningarna för Redovisning i scenariot")</span><span class="sxs-lookup"><span data-stu-id="da93f-131">![G/L Setup in the scenario](media/helene/TechArticleAdjustcost4.png "G/L Setup in the scenario")</span></span>

 <span data-ttu-id="da93f-132">Första tillåtna bokföringsdatum är det datum som anges i fältet Tillåt bokföring från: 10 September 2013.</span><span class="sxs-lookup"><span data-stu-id="da93f-132">First allowed posting date is the date stated in field Allow Posting From: September 10th, 2013.</span></span>  

 <span data-ttu-id="da93f-133">Om såväl lagerperioder som tillåtna bokföringsdatum i Redovisningsinställningar har angetts, kommer det senare av de två att bestämma det tillåtna datumspannet för bokföring.</span><span class="sxs-lookup"><span data-stu-id="da93f-133">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will define the allowed posting date range.</span></span>  

 <span data-ttu-id="da93f-134">Steg 3: Fördelning av ett tillåtet bokföringsdatum.</span><span class="sxs-lookup"><span data-stu-id="da93f-134">Step 3: Assignment of an allowed posting date;</span></span>  

 <span data-ttu-id="da93f-135">Det ursprungliga tilldelade bokföringsdatumet var den 6 september, vilket visas i steg 1.</span><span class="sxs-lookup"><span data-stu-id="da93f-135">The initial assigned Posting Date was September 6th as illustrated in step 1.</span></span> <span data-ttu-id="da93f-136">I det andra steget identifierar emellertid batchjobbet Justera kostn. – Artikeltrans att det tidigast tillåtna bokföringsdatumet är den 10 september och tilldelar därmed den 10 september till justeringsvärdetransaktionen nedan.</span><span class="sxs-lookup"><span data-stu-id="da93f-136">However, in the 2nd step the Adjust Cost – Item entries batch job identifies that earliest allowed Posting Date is September 10th and thereby assigns September 10th to the Adjustment Value Entry, below.</span></span>  

 <span data-ttu-id="da93f-137">![Status för värdetransaktioner i scenariot 2](media/helene/TechArticleAdjustcost5.png "Status för värdetransaktioner i scenariot 2")</span><span class="sxs-lookup"><span data-stu-id="da93f-137">![State of value entries in the scenario 2](media/helene/TechArticleAdjustcost5.png "State of value entries in the scenario 2")</span></span>

 <span data-ttu-id="da93f-138">Vi har nu gått igenom hur man tilldelar bokföringsdatum för värdetransaktioner som skapats genom batchjobbet Justera kost. - artikeltrans.</span><span class="sxs-lookup"><span data-stu-id="da93f-138">We have now reviewed the concept for assigning Posting Dates to Value Entries created by the Adjust Cost - Item entries batch job.</span></span>  

 <span data-ttu-id="da93f-139">Vi fortsätter nu med att granska några scenarier som vi i supportteamet då och då stöter på i samband med tilldelade boföringsdatum i batchjobbet Justera kost. - artikeltrans och relaterade inställningar.</span><span class="sxs-lookup"><span data-stu-id="da93f-139">Let’s continue to review some scenarios that we in the support team comes across from time to time in relation to assigned Posting Dates in the Adjust Cost – Item entries batch job and related setups.</span></span>  

## <a name="scenarios"></a><span data-ttu-id="da93f-140">Scenarierna</span><span class="sxs-lookup"><span data-stu-id="da93f-140">Scenarios</span></span>  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a><span data-ttu-id="da93f-141">Scenario I: "Bokföringsdatumet är inte inom ditt tillåtna intervall för bokföringsdatum..."</span><span class="sxs-lookup"><span data-stu-id="da93f-141">Scenario I: “Posting Date is not within your range of allowed posting dates…”</span></span>  
 <span data-ttu-id="da93f-142">Dett är ett scenario där en användare får nämnda felmeddelande när batch-jobbet Justera kost. - artikeltrans körs.</span><span class="sxs-lookup"><span data-stu-id="da93f-142">This is a scenario where a user is experiencing mentioned error message when the Adjust Cost – Item entries batch job is run.</span></span>  

 <span data-ttu-id="da93f-143">I föregående avsnitt, som beskrev begreppet att tilldela bokföringsdatum, var syftet med batch-jobbet Justera kost. - artikeltrans att skapa en Värdetransaktion med bokföringsdatum 10 september.</span><span class="sxs-lookup"><span data-stu-id="da93f-143">In the previous section, describing the concept of assigning posting dates, the intention of the Adjust Cost – Item entries batch job is to create a Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="da93f-144">![Felmeddelande om bokföringsdatum](media/helene/TechArticleAdjustcost6.png "Felmeddelande om bokföringsdatum")</span><span class="sxs-lookup"><span data-stu-id="da93f-144">![Error message about posting date](media/helene/TechArticleAdjustcost6.png "Error message about posting date")</span></span>

 <span data-ttu-id="da93f-145">Vi följer upp användarinställningarna:</span><span class="sxs-lookup"><span data-stu-id="da93f-145">We follow up on the User Setup:</span></span>  

<span data-ttu-id="da93f-146">![Användarens tillåtna inställning av bokföringsdatum](media/helene/TechArticleAdjustcost7.png "Användarens tillåtna inställning av bokföringsdatum")</span><span class="sxs-lookup"><span data-stu-id="da93f-146">![User's allowed posting dates setup](media/helene/TechArticleAdjustcost7.png "User's allowed posting dates setup")</span></span>

 <span data-ttu-id="da93f-147">Användaren i detta exempel har ett tillåtet datumintervall för bokföring från den 11 september till den 30 september, och får därmed inte bokföra justeringsvärdetransaktionen med bokföringsdatum 10 september.</span><span class="sxs-lookup"><span data-stu-id="da93f-147">The user in this case has an allowed posting date range from September 11th to September 30th and is thereby not allowed to post the Adjustment Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="da93f-148">![Översikt över berörd inställning av bokföringsdatum](media/helene/TechArticleAdjustcost8.png "Översikt över berörd inställning av bokföringsdatum")</span><span class="sxs-lookup"><span data-stu-id="da93f-148">![Overview of involved posting date setup](media/helene/TechArticleAdjustcost8.png "Overview of involved posting date setup")</span></span>

 <span data-ttu-id="da93f-149">Kunskapsbasartikel [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) beskriver ytterligare scenarion relaterade till nämnda felmeddelande.</span><span class="sxs-lookup"><span data-stu-id="da93f-149">Knowledge Base article [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) discusses additional scenarios related to mentioned error message.</span></span>  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a><span data-ttu-id="da93f-150">Scenario II: Bokföringsdatum på justeringsvärdetransaktionen jämfört med bokföringsdatum för transaktionen som orsakar justeringen, till exempel omvärdering eller artikelomkostnad.</span><span class="sxs-lookup"><span data-stu-id="da93f-150">Scenario II: Posting Date on Adjustment Value Entry versus Posting Date on entry causing the adjustment such as Revaluation or Item charge.</span></span>  

### <a name="revaluation-scenario"></a><span data-ttu-id="da93f-151">Omvärderingsscenario:</span><span class="sxs-lookup"><span data-stu-id="da93f-151">Revaluation scenario:</span></span>  
 <span data-ttu-id="da93f-152">Förutsättningar:</span><span class="sxs-lookup"><span data-stu-id="da93f-152">Prerequisites:</span></span>  

 <span data-ttu-id="da93f-153">Lagerinställningar:</span><span class="sxs-lookup"><span data-stu-id="da93f-153">Inventory setup:</span></span>  

-   <span data-ttu-id="da93f-154">Automatisk kostnadsbokföring = Ja</span><span class="sxs-lookup"><span data-stu-id="da93f-154">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="da93f-155">Automatisk kostnadsjustering = Alltid</span><span class="sxs-lookup"><span data-stu-id="da93f-155">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="da93f-156">Genoms. kost.ber.typ = artikel</span><span class="sxs-lookup"><span data-stu-id="da93f-156">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="da93f-157">Period för genomsnittskostnad = Dag</span><span class="sxs-lookup"><span data-stu-id="da93f-157">Average Cost Period=Day</span></span>  

 <span data-ttu-id="da93f-158">Redovisningsinställningar:</span><span class="sxs-lookup"><span data-stu-id="da93f-158">General Ledger Setup:</span></span>  

-   <span data-ttu-id="da93f-159">Tillåt bokföring från = 1 januari 2014</span><span class="sxs-lookup"><span data-stu-id="da93f-159">Allow Posting From = January 1st, 2014</span></span>  

-   <span data-ttu-id="da93f-160">Tillåt bokföring t.o.m. = tom</span><span class="sxs-lookup"><span data-stu-id="da93f-160">Allow Posting To = empty</span></span>  

 <span data-ttu-id="da93f-161">Användarinställningar:</span><span class="sxs-lookup"><span data-stu-id="da93f-161">User Setup:</span></span>  

-   <span data-ttu-id="da93f-162">Tillåt bokföring från = 1 januari 2013.</span><span class="sxs-lookup"><span data-stu-id="da93f-162">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="da93f-163">Tillåt bokföring t.o.m. = tom</span><span class="sxs-lookup"><span data-stu-id="da93f-163">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="da93f-164">För att testa scenariot</span><span class="sxs-lookup"><span data-stu-id="da93f-164">To test the scenario</span></span>  

1.  <span data-ttu-id="da93f-165">Skapa artikel TEST:</span><span class="sxs-lookup"><span data-stu-id="da93f-165">Create item TEST:</span></span>  

     <span data-ttu-id="da93f-166">Basenhet = ST</span><span class="sxs-lookup"><span data-stu-id="da93f-166">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="da93f-167">Kostnad = Genomsnitt</span><span class="sxs-lookup"><span data-stu-id="da93f-167">Costing Method = Average</span></span>  

     <span data-ttu-id="da93f-168">Markera valfria bokföringsmallar.</span><span class="sxs-lookup"><span data-stu-id="da93f-168">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="da93f-169">Öppna artikeljournalen, skapa och bokför en rad så här:</span><span class="sxs-lookup"><span data-stu-id="da93f-169">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="da93f-170">Bokföringsdatum = 15 December 2013</span><span class="sxs-lookup"><span data-stu-id="da93f-170">Posting Date = December 15th, 2013</span></span>  

     <span data-ttu-id="da93f-171">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="da93f-171">Item = TEST</span></span>  

     <span data-ttu-id="da93f-172">Trans.typ = Köp</span><span class="sxs-lookup"><span data-stu-id="da93f-172">Entry Type = Purchase</span></span>  

     <span data-ttu-id="da93f-173">Antal = 100</span><span class="sxs-lookup"><span data-stu-id="da93f-173">Quantity = 100</span></span>  

     <span data-ttu-id="da93f-174">A-pris = 10</span><span class="sxs-lookup"><span data-stu-id="da93f-174">Unit Amount = 10</span></span>  

3.  <span data-ttu-id="da93f-175">Öppna artikeljournalen, skapa och bokför en rad så här:</span><span class="sxs-lookup"><span data-stu-id="da93f-175">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="da93f-176">Datum = 20 december 2013</span><span class="sxs-lookup"><span data-stu-id="da93f-176">Date = December 20th, 2013</span></span>  

     <span data-ttu-id="da93f-177">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="da93f-177">Item = TEST</span></span>  

     <span data-ttu-id="da93f-178">Trans.typ = Negativ justering</span><span class="sxs-lookup"><span data-stu-id="da93f-178">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="da93f-179">Antal = 2</span><span class="sxs-lookup"><span data-stu-id="da93f-179">Quantity = 2</span></span>  

4.  <span data-ttu-id="da93f-180">Öppna artikeljournalen, skapa och bokför en rad så här:</span><span class="sxs-lookup"><span data-stu-id="da93f-180">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="da93f-181">Datum = 15 januari 2014</span><span class="sxs-lookup"><span data-stu-id="da93f-181">Date = January 15th, 2014</span></span>  

     <span data-ttu-id="da93f-182">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="da93f-182">Item = TEST</span></span>  

     <span data-ttu-id="da93f-183">Trans.typ = Negativ justering</span><span class="sxs-lookup"><span data-stu-id="da93f-183">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="da93f-184">Antal = 3</span><span class="sxs-lookup"><span data-stu-id="da93f-184">Quantity = 3</span></span>  

5.  <span data-ttu-id="da93f-185">Öppna omvärderingsjournalen, skapa och bokför en rad så här:</span><span class="sxs-lookup"><span data-stu-id="da93f-185">Open Revaluation Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="da93f-186">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="da93f-186">Item = TEST</span></span>  

     <span data-ttu-id="da93f-187">Kopplas till löpnr = välj den inköpstransaktion som bokförts i steg 2.</span><span class="sxs-lookup"><span data-stu-id="da93f-187">Applies-to Entry = select Purchase entry posted at step 2.</span></span> <span data-ttu-id="da93f-188">Bokföringsdatum för omvärderingen ska vara detsamma som den transaktionen som den justerar.</span><span class="sxs-lookup"><span data-stu-id="da93f-188">The Posting Date of the revaluation will be the same as the entry it adjusts.</span></span>  

     <span data-ttu-id="da93f-189">Styckkostnad (omvärderad) = 40</span><span class="sxs-lookup"><span data-stu-id="da93f-189">Unit Cost Revalued = 40</span></span>  

 <span data-ttu-id="da93f-190">Följande artikeltransaktioner och värdetransaktioner har bokförts:</span><span class="sxs-lookup"><span data-stu-id="da93f-190">The following Item Ledger and Value Entries have been posted:</span></span>  

<span data-ttu-id="da93f-191">![Översikt över resulterande redovisnings- och artikeltransaktioner 1](media/helene/TechArticleAdjustcost9.png "Översikt över resulterande redovisnings- och artikeltransaktioner 1")</span><span class="sxs-lookup"><span data-stu-id="da93f-191">![Overview of resulting item ledger and value entries 1](media/helene/TechArticleAdjustcost9.png "Overview of resulting item ledger and value entries 1")</span></span>

 <span data-ttu-id="da93f-192">![Översikt över resulterande redovisnings- och artikeltransaktioner 2](media/helene/TechArticleAdjustcost10.png "Översikt över resulterande redovisnings- och artikeltransaktioner 2")</span><span class="sxs-lookup"><span data-stu-id="da93f-192">![Overview of resulting item ledger and value entries 2](media/helene/TechArticleAdjustcost10.png "Overview of resulting item ledger and value entries 2")</span></span>

 <span data-ttu-id="da93f-193">Batchjobbet Justera kost. - artikeltrans har identifierat en ändring i kostnad och justerat de negativa justeringarna.</span><span class="sxs-lookup"><span data-stu-id="da93f-193">The Adjust Cost – Item entries batch job has recognized a change in cost and adjusted the Negative Adjustments.</span></span>  

 <span data-ttu-id="da93f-194">**Granskning av bokföringsdatum på skapade justeringsvärdetransaktioner:** Tidigast tillåtna bokföringsdatum som batchjobbet Justera kost. - artikeltrans måste beakta är den 1 januari 2014, vilket anges i redovisningsinställningarna.</span><span class="sxs-lookup"><span data-stu-id="da93f-194">**Review of Posting Dates on created Adjustment Value Entries:** The earliest allowed Posting Date the Adjust Cost - Item Entries batch job has to relate to is January 1st, 2014 as stated in the General Ledger Setup.</span></span>  

 <span data-ttu-id="da93f-195">**Negativ justering i steg 3:** tilldelat bokföringsdatum är den 1 januari 1, vilket anges i redovisningsinställningarna.</span><span class="sxs-lookup"><span data-stu-id="da93f-195">**Negative Adjustment in step 3:** assigned Posting Date is January 1st, provided by General Ledger Setup.</span></span> <span data-ttu-id="da93f-196">Bokföringsdatum för den värdetransaktion som ska omfattas av justering är den 20 december 2013.</span><span class="sxs-lookup"><span data-stu-id="da93f-196">The Posting Date of the Value Entry in scope for adjustment is December 20, 2013.</span></span> <span data-ttu-id="da93f-197">Enligt redovisningsinställningarna ligger datumet inte inom tillåtet datumintervall för bokföring.</span><span class="sxs-lookup"><span data-stu-id="da93f-197">According to General Ledger Setup the date is not within allowed posting date range.</span></span> <span data-ttu-id="da93f-198">Därför tilldelas det bokföringsdatum som anges i fältet Tillåt bokföring fr.o.m i Redovisningsinställningar till justeringsvärdetransaktionen.</span><span class="sxs-lookup"><span data-stu-id="da93f-198">Therefore the Posting Date stated in the Allow Posting From field in the General Ledger Setup is assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="da93f-199">**Negativ justering i steg 4:** tilldelat bokföringsdatum är den 15 januari.</span><span class="sxs-lookup"><span data-stu-id="da93f-199">**Negative Adjustment in step 4:** assigned Posting Date is January 15th.</span></span> <span data-ttu-id="da93f-200">Värdetransaktionen som omfattas av justering har bokföringsdatum 15 januari, vilket ligger inom intervallet för tillåten bokföring enligt redovisningsinställningarna.</span><span class="sxs-lookup"><span data-stu-id="da93f-200">The Value Entry in scope of adjustment has Posting Date January 15th, which is within the allowed posting date range according to General Ledger Setup.</span></span>  

 <span data-ttu-id="da93f-201">Justeringen för den negativa justeringen i steg 3 förorsakar diskussion.</span><span class="sxs-lookup"><span data-stu-id="da93f-201">The adjustment made for the Negative Adjustment in step 3 causes discussion.</span></span> <span data-ttu-id="da93f-202">Ett bättre bokföringsdatum för justeringsvärdetransaktionen hade varit den 20 december eller åtminstone i december, detta eftersom den omvärderingen som förorsakar ändringen i KSV bokfördes i december.</span><span class="sxs-lookup"><span data-stu-id="da93f-202">The favorable Posting Date for the Adjustment Value Entry would have been December 20th or at least within December as the revaluation causing the change in COGS was posted in December.</span></span>  

 <span data-ttu-id="da93f-203">För att uppnå en decemberjustering av den negativa justeringen i steg 3 måste Redovisningsinställningar, fältet Tillåt bokföring fr.o.m, ange ett datum i december.</span><span class="sxs-lookup"><span data-stu-id="da93f-203">To achieve adjustment in December of the Negative Adjustment in step 3, the General Ledger Setup, Allow Posting From field, need to state a date in December.</span></span>  

 <span data-ttu-id="da93f-204">**Sammanfattning:**</span><span class="sxs-lookup"><span data-stu-id="da93f-204">**Conclusion:**</span></span>  

 <span data-ttu-id="da93f-205">Med erfarenheterna från detta scenario i ryggen och i beaktande av de lämpligaste inställningarna för tillåtet datumintervall för bokföring för ett företag, kan följande komma till nytta: Så länge ändringar i lagervärde får bokföras inom en period (i detta fall december) bör de inställningar som företaget använder för tillåtna bokföringsintervall justeras i enlighet med detta beslut.</span><span class="sxs-lookup"><span data-stu-id="da93f-205">With the experiences from this scenario, considering most suitable setup of allowed posting date range for a company, the following might be useful: As long as changes in inventory value is allowed to be posted in a period, December in this case, the setup the company uses for allowed posting date ranges should be aligned with this decision.</span></span> <span data-ttu-id="da93f-206">Fältet Tillåt bokföring fr.o.m i Redovisningsinställningarna, som anger att den 1 december skulle låta omvärderingen utförd i december vidarebefordras till att påverka utgående transaktioner under samma period.</span><span class="sxs-lookup"><span data-stu-id="da93f-206">The Allow Posting From in the General Ledger Setup, stating December 1st  would allow the revaluation made in December to be forwarded to affected outbound entries in the same period.</span></span>  

 <span data-ttu-id="da93f-207">Användargrupper är inte behöriga att bokföra i december utan i januari, vilket troligen var avsett att begränsas av Redovisningsinställningarna i detta scenario, bör i stället tas upp via användarinställningarna.</span><span class="sxs-lookup"><span data-stu-id="da93f-207">User groups not allowed to post in December but in January, which was probably intended to be limited by the General Ledger Setup in this scenario, should instead be addressed via the User setup.</span></span>  

### <a name="item-charge-scenario"></a><span data-ttu-id="da93f-208">Artikelomkostnadsscenario:</span><span class="sxs-lookup"><span data-stu-id="da93f-208">Item charge scenario:</span></span>  
 <span data-ttu-id="da93f-209">Förutsättningar:</span><span class="sxs-lookup"><span data-stu-id="da93f-209">Prerequisites:</span></span>  

 <span data-ttu-id="da93f-210">Lagerinställningar:</span><span class="sxs-lookup"><span data-stu-id="da93f-210">Inventory setup:</span></span>  

-   <span data-ttu-id="da93f-211">Automatisk kostnadsbokföring = Ja</span><span class="sxs-lookup"><span data-stu-id="da93f-211">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="da93f-212">Automatisk kostnadsjustering = Alltid</span><span class="sxs-lookup"><span data-stu-id="da93f-212">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="da93f-213">Genoms. kost.ber.typ = artikel</span><span class="sxs-lookup"><span data-stu-id="da93f-213">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="da93f-214">Period för genomsnittskostnad = Dag</span><span class="sxs-lookup"><span data-stu-id="da93f-214">Average Cost Period=Day</span></span>  

 <span data-ttu-id="da93f-215">Redovisningsinställningar:</span><span class="sxs-lookup"><span data-stu-id="da93f-215">General Ledger Setup:</span></span>  

-   <span data-ttu-id="da93f-216">Tillåt bokföring från = 1 januari 2013.</span><span class="sxs-lookup"><span data-stu-id="da93f-216">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="da93f-217">Tillåt bokföring t.o.m. = tom</span><span class="sxs-lookup"><span data-stu-id="da93f-217">Allow Posting To = empty</span></span>  

 <span data-ttu-id="da93f-218">Användarinställningar:</span><span class="sxs-lookup"><span data-stu-id="da93f-218">User Setup:</span></span>  

-   <span data-ttu-id="da93f-219">Tillåt bokföring från = 1 januari 2013.</span><span class="sxs-lookup"><span data-stu-id="da93f-219">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="da93f-220">Tillåt bokföring t.o.m. = tom</span><span class="sxs-lookup"><span data-stu-id="da93f-220">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="da93f-221">För att testa scenariot</span><span class="sxs-lookup"><span data-stu-id="da93f-221">To test the scenario</span></span>  

1.  <span data-ttu-id="da93f-222">Skapa artikelomkostnad:</span><span class="sxs-lookup"><span data-stu-id="da93f-222">Create item charge:</span></span>  

     <span data-ttu-id="da93f-223">Basenhet = ST</span><span class="sxs-lookup"><span data-stu-id="da93f-223">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="da93f-224">Kostnad = Genomsnitt</span><span class="sxs-lookup"><span data-stu-id="da93f-224">Costing Method = Average</span></span>  

     <span data-ttu-id="da93f-225">Markera valfria bokföringsmallar.</span><span class="sxs-lookup"><span data-stu-id="da93f-225">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="da93f-226">Skapa en ny inköpsorder</span><span class="sxs-lookup"><span data-stu-id="da93f-226">Create new purchase order</span></span>  

     <span data-ttu-id="da93f-227">Inköpsleverantörsnr: 10000</span><span class="sxs-lookup"><span data-stu-id="da93f-227">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="da93f-228">Bokföringsdatum = 15 December 2013</span><span class="sxs-lookup"><span data-stu-id="da93f-228">Posting Date = December 15th, 2013</span></span>  

     <span data-ttu-id="da93f-229">Leverantörens fakturanr: 1234</span><span class="sxs-lookup"><span data-stu-id="da93f-229">Vendor Invoice No.: 1234</span></span>  

     <span data-ttu-id="da93f-230">På inköpsorderraden:</span><span class="sxs-lookup"><span data-stu-id="da93f-230">On the purchase order line:</span></span>  

     <span data-ttu-id="da93f-231">Artikel = DEBITERING</span><span class="sxs-lookup"><span data-stu-id="da93f-231">Item = CHARGE</span></span>  

     <span data-ttu-id="da93f-232">Antal = 1</span><span class="sxs-lookup"><span data-stu-id="da93f-232">Quantity = 1</span></span>  

     <span data-ttu-id="da93f-233">Inköpspris (BVA) = 100</span><span class="sxs-lookup"><span data-stu-id="da93f-233">Direct Unit Cost = 100</span></span>  

     <span data-ttu-id="da93f-234">Bokför Inleverera och Fakturera.</span><span class="sxs-lookup"><span data-stu-id="da93f-234">Post Receive and Invoice.</span></span>  

3.  <span data-ttu-id="da93f-235">Skapa en ny försäljningsorder:</span><span class="sxs-lookup"><span data-stu-id="da93f-235">Create new sales order:</span></span>  

     <span data-ttu-id="da93f-236">Förs.kundnr: 10000</span><span class="sxs-lookup"><span data-stu-id="da93f-236">Sell-to Customer No.: 10000</span></span>  

     <span data-ttu-id="da93f-237">Bokföringsdatum = 16 december 2013</span><span class="sxs-lookup"><span data-stu-id="da93f-237">Posting Date = December 16th, 2013</span></span>  

     <span data-ttu-id="da93f-238">På försäljningsorderraden:</span><span class="sxs-lookup"><span data-stu-id="da93f-238">On the sales order line:</span></span>  

     <span data-ttu-id="da93f-239">Artikel = DEBITERING</span><span class="sxs-lookup"><span data-stu-id="da93f-239">Item = CHARGE</span></span>  

     <span data-ttu-id="da93f-240">Antal = 1</span><span class="sxs-lookup"><span data-stu-id="da93f-240">Quantity = 1</span></span>  

     <span data-ttu-id="da93f-241">A-pris = 135</span><span class="sxs-lookup"><span data-stu-id="da93f-241">Unit Price = 135</span></span>  

     <span data-ttu-id="da93f-242">Bokför leverans och faktura.</span><span class="sxs-lookup"><span data-stu-id="da93f-242">Post Ship and Invoice.</span></span>  

4.  <span data-ttu-id="da93f-243">Redovisningsinställningar:</span><span class="sxs-lookup"><span data-stu-id="da93f-243">General Ledger Setup:</span></span>  

     <span data-ttu-id="da93f-244">Tillåt bokföring från = 1 januari 2014</span><span class="sxs-lookup"><span data-stu-id="da93f-244">Allow Posting From = January 1st, 2014</span></span>  

     <span data-ttu-id="da93f-245">Tillåt bokföring t.o.m. = tom</span><span class="sxs-lookup"><span data-stu-id="da93f-245">Allow Posting To = blank</span></span>  

5.  <span data-ttu-id="da93f-246">Skapa en ny inköpsorder:</span><span class="sxs-lookup"><span data-stu-id="da93f-246">Create new purchase order:</span></span>  

     <span data-ttu-id="da93f-247">Inköpsleverantörsnr: 10000</span><span class="sxs-lookup"><span data-stu-id="da93f-247">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="da93f-248">Bokföringsdatum = 2 januari 2014</span><span class="sxs-lookup"><span data-stu-id="da93f-248">Posting Date = January 2nd, 2014</span></span>  

     <span data-ttu-id="da93f-249">Leverantörens fakturanr: 2345</span><span class="sxs-lookup"><span data-stu-id="da93f-249">Vendor Invoice No.: 2345</span></span>  

     <span data-ttu-id="da93f-250">På inköpsorderraden:</span><span class="sxs-lookup"><span data-stu-id="da93f-250">On the purchase order line:</span></span>  

     <span data-ttu-id="da93f-251">Artikelomkostnad = JB-FRAKT</span><span class="sxs-lookup"><span data-stu-id="da93f-251">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="da93f-252">Antal = 1</span><span class="sxs-lookup"><span data-stu-id="da93f-252">Quantity = 1</span></span>  

     <span data-ttu-id="da93f-253">Inköpspris (BVA) = 3</span><span class="sxs-lookup"><span data-stu-id="da93f-253">Direct Unit Cost = 3</span></span>  

     <span data-ttu-id="da93f-254">Tilldela artikelomkostnader till inleverans från steg 2.</span><span class="sxs-lookup"><span data-stu-id="da93f-254">Assign Item Charge to Purchase Receipt from step 2.</span></span>  

     <span data-ttu-id="da93f-255">Bokför inleverans och faktura.</span><span class="sxs-lookup"><span data-stu-id="da93f-255">Post Receipt and Invoice.</span></span>  

     <span data-ttu-id="da93f-256">![Översikt över resulterande redovisnings- och artikeltransaktioner 3](media/helene/TechArticleAdjustcost11.png "Översikt över resulterande redovisnings- och artikeltransaktioner 3")</span><span class="sxs-lookup"><span data-stu-id="da93f-256">![Overview of resulting item ledger and value entries 3](media/helene/TechArticleAdjustcost11.png "Overview of resulting item ledger and value entries 3")</span></span>

6.  <span data-ttu-id="da93f-257">Arbetsdagen 3 januari anländer en inköpsfaktura med ytterligare artikelomkostnader till inköpet i steg 2.</span><span class="sxs-lookup"><span data-stu-id="da93f-257">On work date January 3rd a purchase invoice arrives, containing an additional item charge to the purchase made in step 2.</span></span> <span data-ttu-id="da93f-258">Fakturan har den dokumentdatumet den 30 december och bokförs därför med bokföringsdatum 30 december 2013.</span><span class="sxs-lookup"><span data-stu-id="da93f-258">This invoice has document date December 30th and is therefore posted with Posting Date December 30th, 2013.</span></span>  

     <span data-ttu-id="da93f-259">Skapa en ny inköpsorder:</span><span class="sxs-lookup"><span data-stu-id="da93f-259">Create new purchase order:</span></span>  

     <span data-ttu-id="da93f-260">Inköpsleverantörsnr: 10000</span><span class="sxs-lookup"><span data-stu-id="da93f-260">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="da93f-261">Bokföringsdatum = 30 december 2013</span><span class="sxs-lookup"><span data-stu-id="da93f-261">Posting Date = December 30th, 2013</span></span>  

     <span data-ttu-id="da93f-262">Leverantörens fakturanr: 3456</span><span class="sxs-lookup"><span data-stu-id="da93f-262">Vendor Invoice No.: 3456</span></span>  

     <span data-ttu-id="da93f-263">På inköpsorderraden:</span><span class="sxs-lookup"><span data-stu-id="da93f-263">On the purchase order line:</span></span>  

     <span data-ttu-id="da93f-264">Artikelomkostnad = JB-FRAKT</span><span class="sxs-lookup"><span data-stu-id="da93f-264">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="da93f-265">Antal = 1</span><span class="sxs-lookup"><span data-stu-id="da93f-265">Quantity = 1</span></span>  

     <span data-ttu-id="da93f-266">Inköpspris (BVA) = 2</span><span class="sxs-lookup"><span data-stu-id="da93f-266">Direct Unit Cost = 2</span></span>  

     <span data-ttu-id="da93f-267">Tilldela artikelomkostnader till inleverans från steg 2.</span><span class="sxs-lookup"><span data-stu-id="da93f-267">Assign Item Charge to Purchase Receipt from step 2</span></span>  

     <span data-ttu-id="da93f-268">Bokför inleverans och faktura.</span><span class="sxs-lookup"><span data-stu-id="da93f-268">Post Receipt and Invoice.</span></span>  

   <span data-ttu-id="da93f-269">![Översikt över resulterande redovisnings- och artikeltransaktioner 4](media/helene/TechArticleAdjustcost12.png "Översikt över resulterande redovisnings- och artikeltransaktioner 4")</span><span class="sxs-lookup"><span data-stu-id="da93f-269">![Overview of resulting item ledger and value entries 4](media/helene/TechArticleAdjustcost12.png "Overview of resulting item ledger and value entries 4")</span></span>

 <span data-ttu-id="da93f-270">Rapporten Lagervärdering skrivs ut per den 31 december 2013</span><span class="sxs-lookup"><span data-stu-id="da93f-270">Inventory Valuation report is printed as of Date December 31st , 2013</span></span>  

<span data-ttu-id="da93f-271">![Innehåll i rapporten Lagervärdering](media/helene/TechArticleAdjustcost13.png "Innehåll i rapporten Lagervärdering")</span><span class="sxs-lookup"><span data-stu-id="da93f-271">![Content of the Inventory Valuation report](media/helene/TechArticleAdjustcost13.png "Content of the Inventory Valuation report")</span></span>

 <span data-ttu-id="da93f-272">**Summering av scenario:**</span><span class="sxs-lookup"><span data-stu-id="da93f-272">**Summary of scenario:**</span></span>  

 <span data-ttu-id="da93f-273">Beskrivet scenario erhåller i slutändan en lagervärderingsrapport som visar antalet = 0 när värdet = 2.</span><span class="sxs-lookup"><span data-stu-id="da93f-273">The described scenario ends up with an Inventory Valuation report demonstrating Quantity = 0 while the Value = 2.</span></span> <span data-ttu-id="da93f-274">Artikelomkostnaden som bokfördes i steg 11 är en del av värdet Lagerökning för december, medan lagerminskningen för samma period inte påverkas.</span><span class="sxs-lookup"><span data-stu-id="da93f-274">The Item charge posted in step 11 is part of the Inventory Increase value of December while the Inventory Decrease of the same period is not affected.</span></span>  

 <span data-ttu-id="da93f-275">Att låta redovisningsinställningarna ange Tillåt bokföring fr.o.m den 1 januari var användbart för den första artikelomkostnaden.</span><span class="sxs-lookup"><span data-stu-id="da93f-275">Having the General Ledger Setup stating Allow Posting From January 1st was a good thing for the first Item charge.</span></span> <span data-ttu-id="da93f-276">Kostnaderna för ökat och minskat lager registrerades under samma period.</span><span class="sxs-lookup"><span data-stu-id="da93f-276">The costs of the Inventory Increase and Decrease was recorded in the same period.</span></span> <span data-ttu-id="da93f-277">För den andra artikelomkostnaden gör emellertid redovisningsinställningarna att ändringen i KSV bokförs under nästkommande period.</span><span class="sxs-lookup"><span data-stu-id="da93f-277">For the second Item charge however, the General Ledger Setup causes the change in COGS to be recognized in the period after.</span></span>  

 <span data-ttu-id="da93f-278">**Sammanfattning:**</span><span class="sxs-lookup"><span data-stu-id="da93f-278">**Conclusion:**</span></span>  

 <span data-ttu-id="da93f-279">Det är svårt att låta rapporten Lagerutvärdering visa kvantiteten = 0 när värdet är <> 0.</span><span class="sxs-lookup"><span data-stu-id="da93f-279">It’s a challenge to have the Inventory Valuation report to demonstrate Quantity = 0 while the Value <> 0.</span></span> <span data-ttu-id="da93f-280">I detta fall är det också svårare att uttrycka de optimala inställningarna då inköpsfakturorna anländer samma dag men adresserar olika perioder eller till och med räkenskapsår.</span><span class="sxs-lookup"><span data-stu-id="da93f-280">In this case it’s also more difficult to express the optimal settings, having purchase invoices arriving the same day but addressing different periods or even fiscal years.</span></span> <span data-ttu-id="da93f-281">Att flytta fram till ett nytt räkenskapsår kräver vanligtvis lite planering, och som ett led i insikten för transaktionsprocessen Justera kost. - artikeltrans måste KSV-detektering beaktas.</span><span class="sxs-lookup"><span data-stu-id="da93f-281">Crossing to a new fiscal year usually requires some planning and as part of that the insight of Adjust Cost – Item entries process, recognizing COGS, is to be considered.</span></span>  

 <span data-ttu-id="da93f-282">I detta scenario kunde ett alternativ vara att låta Redovisningsinställningarna, fältet Tillåt bokföring fr.o.m att ange ett datum i december några dagar längre fram, samt att flytta fram bokföringen av den första artikelomkostnaden, detta i syfte att låta alla kostnader för föregående period/räkenskapsår först registreras för den period som de tillhör, köra batch-jobbet Justera kostn. - artikeltrans. och därefter flytta tillåtet bokföringsdatum till den nya perioden\/det nya räkenskapsåret.</span><span class="sxs-lookup"><span data-stu-id="da93f-282">In this scenario one option could have been to have the General Ledger Setup, field Allow Posting From, stating a date in December for a couple of more days and the posting of the first item charge postponed to allow all costs for the previous period/fiscal year to be recognized for the period they belong to first, having the Adjust Cost – Item entries batch job run and thereafter move the allowed posting date to the new period\/fiscal year.</span></span> <span data-ttu-id="da93f-283">Därefter kan den artikelomkostnaden med bokföringsdatum 2 januari bokföras.</span><span class="sxs-lookup"><span data-stu-id="da93f-283">The first item charge with posting date January 2nd could then be posted.</span></span>  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a><span data-ttu-id="da93f-284">Historik för batch-jobbet Justera kost. - artikeltrans</span><span class="sxs-lookup"><span data-stu-id="da93f-284">History of Adjust Cost – Item entries batch job</span></span>  
 <span data-ttu-id="da93f-285">Nedan visas en sammanfattning av begreppet Bokföra datum för justeringsvärdetransaktioner utförda av batch-jobbet Justera kost. - artikeltrans. sedan version 3.0.</span><span class="sxs-lookup"><span data-stu-id="da93f-285">Below is a summary of the concept assigning Posting Dates to Adjustment Value Entries by the Adjust Cost – Item entries batch job since version 3.0.</span></span>  

### <a name="from-version-30370a"></a><span data-ttu-id="da93f-286">Från version 3.0..3.70.A</span><span class="sxs-lookup"><span data-stu-id="da93f-286">From version 3.0..3.70.A</span></span>  
 <span data-ttu-id="da93f-287">I begäranformuläret i batch-jobbet Justera kost. - artikeltrans är finns ett bokföringsdatum som ska anges av användaren.</span><span class="sxs-lookup"><span data-stu-id="da93f-287">In the request form of the Adjust Cost - Item Entries batch job there is a Posting Date to be entered by the user.</span></span> <span data-ttu-id="da93f-288">Batch-jobbet körs genom alla nödvändiga förändringar och skapar värdetransaktioner med det bokföringsdatum som har angetts i formuläret.</span><span class="sxs-lookup"><span data-stu-id="da93f-288">The batch job runs through all necessary changes and creates value entries with the posting date entered in the request form.</span></span> <span data-ttu-id="da93f-289">Föreslaget bokföringsdatum som ska användas är dagens datum.</span><span class="sxs-lookup"><span data-stu-id="da93f-289">Suggested posting date to use is today’s date.</span></span>  

### <a name="version-370b40"></a><span data-ttu-id="da93f-290">Version 3.70.B..4.0</span><span class="sxs-lookup"><span data-stu-id="da93f-290">Version 3.70.B..4.0</span></span>  
 <span data-ttu-id="da93f-291">I begäranformuläret i batch-jobbet Justera kost. - artikeltrans finns ett bokföringsdatum för stängd periodtransaktion som ska anges av användaren.</span><span class="sxs-lookup"><span data-stu-id="da93f-291">In the request form of the Adjust Cost - Item Entries batch job there is a Closed Period Entry Posting Date to be entered by the user.</span></span> <span data-ttu-id="da93f-292">Batch-jobbet körs genom alla nödvändiga ändringar och skapar värdetransaktioner med bokföringsdatumet för den överordnade artikeltransaktionen (leveransdatumet för den försäljning som justeringen adresserar).</span><span class="sxs-lookup"><span data-stu-id="da93f-292">The batch job runs through all necessary changes and creates value entries with the posting date of the parent item ledger entry (shipment date of the sale that the adjustment address).</span></span> <span data-ttu-id="da93f-293">Om bokföringsdatumet för den överordnade artikeltransaktionen inte faller inom det tillåtna bokföringsintervallet, kommer det bokföringsdatum som angetts som bokföringsdatum för stängd periodtransaktion att tilldelas justeringsvärdetransaktionen.</span><span class="sxs-lookup"><span data-stu-id="da93f-293">If the posting date of the parent item ledger entry is not within allowed posting date range the posting date stated as Closed Period Entry Posting Date will be assigned the Adjustment Value Entry.</span></span> <span data-ttu-id="da93f-294">Ett datum anses ligga i en stängd period då det infaller före datumet i fältet Tillåt bokföring fr.o.m i Redovisningsinställningarna.</span><span class="sxs-lookup"><span data-stu-id="da93f-294">A date is considered to be in a closed period when it is earlier than the date in the Allow Posting From field in the General Ledger Setup.</span></span>  

### <a name="from-version-50"></a><span data-ttu-id="da93f-295">Från version 5.0:</span><span class="sxs-lookup"><span data-stu-id="da93f-295">From version 5.0:</span></span>  
 <span data-ttu-id="da93f-296">I batch-jobbet Justera kost. - artikeltrans finns inte längre något bokföringsdatum som måste anges av användaren.</span><span class="sxs-lookup"><span data-stu-id="da93f-296">There is no longer a posting date to be stated in the request form of the Adjust Cost - Item entries batch job.</span></span> <span data-ttu-id="da93f-297">Batch-jobbet körs igenom alla nödvändiga förändringar och skapar värdetransaktioner med samma bokföringsdatum som den värdetransaktion jobbet korrigerar.</span><span class="sxs-lookup"><span data-stu-id="da93f-297">The batch job runs through all necessary changes and creates value entries with the posting date of the value entry it adjusts.</span></span> <span data-ttu-id="da93f-298">Om bokföringsdatumet inte ligger inom tillåtet intervall används bokföringsdatumet i fältet Tillåt bokföring fr.o.m. i Redovisningsinställningarna ELLER, om lagerperioder används, så används det senare datumet av de båda.</span><span class="sxs-lookup"><span data-stu-id="da93f-298">If the posting date is not within allowed posting date range the posting date in the Allow Posting From field in the General Ledger Setup, OR if the Inventory periods are used, the later date of the two will be used.</span></span> <span data-ttu-id="da93f-299">Se begreppsbeskrivningen ovan.</span><span class="sxs-lookup"><span data-stu-id="da93f-299">See described concept above.</span></span>  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a><span data-ttu-id="da93f-300">Historik för Bokför lagerkostnad i redov.</span><span class="sxs-lookup"><span data-stu-id="da93f-300">History of Post Inventory cost to G/L batch job</span></span>  
 <span data-ttu-id="da93f-301">Batch-jobbet Bokför lagerkostnad i redovisning är nära knutet till batch-jobbet Justera kost.-artikeltrans, varför historiken för batch-jobbet även summeras och delas här.</span><span class="sxs-lookup"><span data-stu-id="da93f-301">The Post Inventory Cost to G/L batch job is closely related to the Adjust Cost – Item entries batch job why the history of this batch job is summarized and shared here as well.</span></span>  

### <a name="from-version-30370a"></a><span data-ttu-id="da93f-302">Från version 3.0..3.70.A</span><span class="sxs-lookup"><span data-stu-id="da93f-302">From version 3.0..3.70.A</span></span>  
 <span data-ttu-id="da93f-303">I begäranformuläret i Bokför lagerkostnad i redov. finns ett bokföringsdatum som ska anges av användaren.</span><span class="sxs-lookup"><span data-stu-id="da93f-303">In the request form of the Post Inventory Cost to G/L there is a Posting Date to be entered by the user.</span></span> <span data-ttu-id="da93f-304">Batch-jobbet körs genom alla värdetransaktioner i filtret (om sådana finns) och skapar redovisningstransaktioner med det bokföringsdatum som har angetts i formuläret.</span><span class="sxs-lookup"><span data-stu-id="da93f-304">The batch job runs through all value entries within the filter, if any, and creates General Ledger Entries with Posting Date entered in the request form.</span></span>  

### <a name="version-370b40"></a><span data-ttu-id="da93f-305">Version 3.70.B..4.0</span><span class="sxs-lookup"><span data-stu-id="da93f-305">Version 3.70.B..4.0</span></span>  
 <span data-ttu-id="da93f-306">I begäranformuläret i Bokför lagerkostnad i redov. är finns fältet Bokföringsdatum för stängd periodtransaktion tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="da93f-306">In the request form of the Post Inventory Cost to G/L the Closed Period Entry Posting Date field is available.</span></span> <span data-ttu-id="da93f-307">Programmet använder det datum som du anger i detta fält som bokföringsdatum för de redovisningstransaktioner som skapas för värdetransaktioner vars bokföringsdatum finns i avslutade bokföringsperioder.</span><span class="sxs-lookup"><span data-stu-id="da93f-307">The program uses the date you enter in this field as the posting date for the general ledger entries it creates for value entries whose posting dates are in closed accounting periods.</span></span> <span data-ttu-id="da93f-308">I annat fall kommer redovisningstransaktionerna att ha samma bokföringsdatum som de ursprungliga värdetransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="da93f-308">Otherwise, the general ledger entries will have the same posting date as the original value entries.</span></span> <span data-ttu-id="da93f-309">Ett datum anses ligga i en stängd period då det infaller före datumet i fältet Tillåt bokföring fr.o.m i Redovisningsinställningarna.</span><span class="sxs-lookup"><span data-stu-id="da93f-309">A date is considered to be in a closed period when it is earlier than the date in the Allow Posting From field in the General Ledger Setup.</span></span> <span data-ttu-id="da93f-310">Om du bokför G\/L per bokföringsmall kommer redovisningstransaktionerna att få det bokföringsdatum som har angetts i fältet Bokföringsdatum i formuläret.</span><span class="sxs-lookup"><span data-stu-id="da93f-310">If posting to G\/L Per Posting Group, the general ledger entries will have the posting date that is specified in the Posting Date field in the request form.</span></span>  

 <span data-ttu-id="da93f-311">I version 3 och 4 söker batch-jobbet igenom alla värdetransaktioner i syfte att undersöka om det finns några värdetransaktioner där kost.belopp (faktiskt) skiljer sig från den kostnad som bokförts i redov.</span><span class="sxs-lookup"><span data-stu-id="da93f-311">In version 3 and 4 the batch job scans all value entries to detect if there are any value entries where Cost Amount (Actual) differs from Cost Posted to G/L.</span></span> <span data-ttu-id="da93f-312">Om det finns skillnader kommer skillnaden att bokföras i en redovisningstransaktion.</span><span class="sxs-lookup"><span data-stu-id="da93f-312">If there is a difference detected the differing amount will be posted in a G/L entry.</span></span> <span data-ttu-id="da93f-313">Om förväntad kostnadsbokföring används kommer motsvarande fält att bearbetas på samma sätt.</span><span class="sxs-lookup"><span data-stu-id="da93f-313">If expected cost posting is used corresponding fields are processed in the same way.</span></span>  

<span data-ttu-id="da93f-314">![Faktiska kostnader jämfört med förväntade kostnader](media/helene/TechArticleAdjustcost14.png "Faktiska kostnader jämfört med förväntade kostnader")</span><span class="sxs-lookup"><span data-stu-id="da93f-314">![Actual cost versus expected cost](media/helene/TechArticleAdjustcost14.png "Actual cost versus expected cost")</span></span>

### <a name="from-version-50"></a><span data-ttu-id="da93f-315">Från version 5.0:</span><span class="sxs-lookup"><span data-stu-id="da93f-315">From version 5.0:</span></span>  
 <span data-ttu-id="da93f-316">I batch-jobbet Bokför lagerkostnad i redov. finns inte längre något bokföringsdatum som måste anges i begäranformuläret.</span><span class="sxs-lookup"><span data-stu-id="da93f-316">There is no longer a posting date to be stated in the request form of the Post Inventory Cost to G/L batch job.</span></span> <span data-ttu-id="da93f-317">Bokföringstransaktionen skapas med samma bokföringsdatum som den relaterade värdetransaktionen.</span><span class="sxs-lookup"><span data-stu-id="da93f-317">The G/L entry is created with the same Posting Date as the related value entry.</span></span> <span data-ttu-id="da93f-318">Datumintervall för tillåten bokföring måste tillåta bokföringsdatumet för redovisningstransaktionen som skapats för att avsluta batch-jobbet.</span><span class="sxs-lookup"><span data-stu-id="da93f-318">In order to complete the batch job the allowed posting date range must allow the Posting Date of the created G/L entry.</span></span> <span data-ttu-id="da93f-319">I annat fall måste datumintervallet för tillåten bokföring tillfälligt öppnas igen genom att ändra eller ta bort datumen i fältet Tillåt bokföring fr.o.m och Till i Redovisningsinställningarna.</span><span class="sxs-lookup"><span data-stu-id="da93f-319">If not, the allowed posting date range must be temporarily re-opened by changing or removing the dates in the Allow Posting From and To fields in the General Ledger Setup.</span></span> <span data-ttu-id="da93f-320">För att undvika avstämningsproblem krävs att okföringsdatum för redovisningstransaktionen motsvarar bokföringsdatumet för värdetransaktionen.</span><span class="sxs-lookup"><span data-stu-id="da93f-320">To avoid reconciliation issues it is required that Posting Date of the G/L Entry corresponds to the Posting Date of the Value Entry.</span></span>  

 <span data-ttu-id="da93f-321">Batch-jobbet söker igenom tabellen 5811 - Bokför värdetransaktion i redovisning i syfte att identifiera värdetransaktionerna i omfånget för bokföring i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="da93f-321">The batch job scans Table 5811 - Post Value Entry to G/L, to identify the Value Entries in scope for posting to General Ledger.</span></span> <span data-ttu-id="da93f-322">Tabellen töms efter slutförd körning.</span><span class="sxs-lookup"><span data-stu-id="da93f-322">After successful run the table is emptied.</span></span>

## <a name="see-also"></a><span data-ttu-id="da93f-323">Se även</span><span class="sxs-lookup"><span data-stu-id="da93f-323">See Also</span></span>  
[<span data-ttu-id="da93f-324">Designdetaljer: Lagerkalkylering</span><span class="sxs-lookup"><span data-stu-id="da93f-324">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)  
[<span data-ttu-id="da93f-325">Designdetaljer: Artikelkoppling</span><span class="sxs-lookup"><span data-stu-id="da93f-325">Design Details: Item Application</span></span>](design-details-item-application.md)  
