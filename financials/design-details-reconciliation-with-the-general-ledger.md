---
title: "Designdetaljer: Avstämning med redovisningen | Microsoft Docs"
description: "Det här avsnittet beskriver avstämning med redovisningen när du bokför lagertransaktioner, till exempel försäljningsutleveranser, produktionsutflöde eller negativa justeringar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, reconciliation, general ledger, inventory
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6b45f26f4e9ef63d0bdb6cfe755c0e7a45142483
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-reconciliation-with-the-general-ledger"></a><span data-ttu-id="75947-103">Designdetaljer: Avstämning med redovisningen</span><span class="sxs-lookup"><span data-stu-id="75947-103">Design Details: Reconciliation with the General Ledger</span></span>
<span data-ttu-id="75947-104">När lagertransaktioner bokförs till exempel utleveranser, produktionsutflöde eller negativa justeringar registreras antals- och värdeändringarna i lagret i artikeltransaktionerna respektive värdetransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="75947-104">When you post inventory transactions, such as sales shipments, production output, or negative adjustments, the quantity and value changes to the inventory are recorded in the item ledger entries and the value entries, respectively.</span></span> <span data-ttu-id="75947-105">Nästa steg i processen går ut på att bokföra lagervärdena på redovisningens lagerkonton.</span><span class="sxs-lookup"><span data-stu-id="75947-105">The next step in the process is to post the inventory values to the inventory accounts in the general ledger.</span></span>  

<span data-ttu-id="75947-106">Det finns två sätt att stämma av lagerredovisningen med redovisningen:</span><span class="sxs-lookup"><span data-stu-id="75947-106">There are two ways to reconcile the inventory ledger with the general ledger:</span></span>  

* <span data-ttu-id="75947-107">Manuellt genom att köra batch-jobbet **Bokför lagerkostnad i redov.**.</span><span class="sxs-lookup"><span data-stu-id="75947-107">Manually, by running the **Post Inventory Cost to G/L** batch job.</span></span>  
* <span data-ttu-id="75947-108">Automatiskt, varje gång som du bokför en lagertransaktion.</span><span class="sxs-lookup"><span data-stu-id="75947-108">Automatically, every time that you post an inventory transaction.</span></span>  

## <a name="post-inventory-cost-to-gl-batch-job"></a><span data-ttu-id="75947-109">Batchjobbet Bokför lagerkostnad i redovisning.</span><span class="sxs-lookup"><span data-stu-id="75947-109">Post Inventory Cost to G/L Batch Job</span></span>  
<span data-ttu-id="75947-110">När batch-jobbet **Bokför lagerkostnad i redov.** körs skapas redovisningstransaktionerna utifrån värdetransaktioner.</span><span class="sxs-lookup"><span data-stu-id="75947-110">When you run the **Post Inventory Cost to G/L** batch job, the general ledger entries are created based on value entries.</span></span> <span data-ttu-id="75947-111">Du kan sammanställa redovisningstransaktioner för varje värdetransaktion, eller skapa redovisningstransaktioner för varje kombination av bokföringsdatum, lagerställekod, lagerbokföringsmall, generell rörelsebokföringsmall och generell produktbokföringsmall.</span><span class="sxs-lookup"><span data-stu-id="75947-111">You have the option to summarize general ledger entries for each value entry, or create general ledger entries for each combination of posting date, location code, inventory posting group, general business posting group, and general product posting group.</span></span>  

<span data-ttu-id="75947-112">Bokföringsdatum för redovisningstransaktionerna anges till bokföringsdatumet för motsvarande värdetransaktion, utom när värdetransaktionen infaller i en stängd bokföringsperiod.</span><span class="sxs-lookup"><span data-stu-id="75947-112">The posting dates of the general ledger entries are set to the posting date of the corresponding value entry, except when the value entry falls in a closed accounting period.</span></span> <span data-ttu-id="75947-113">I det här fallet hoppas värdetransaktionen över och du måste ändra antingen redovisningsinställningar eller användarinställningar för att aktivera bokföring i datumintervallet.</span><span class="sxs-lookup"><span data-stu-id="75947-113">In this case, the value entry is skipped, and you must change either the general ledger setup or the user setup to enable posting in the date range.</span></span>  

<span data-ttu-id="75947-114">När du kör batch-jobbet **Bokför lagerkostnad i redov.** kan du få fel på grund av med saknad inställning eller inkompatibel dimensionsinställning.</span><span class="sxs-lookup"><span data-stu-id="75947-114">When you run the **Post Inventory Cost to G/L** batch job, you might receive errors because of missing setup or incompatible dimension setup.</span></span> <span data-ttu-id="75947-115">Om fel uppstår i batch-jobbets dimensionsinställning ersätter den dessa fel och använder dimensionerna för värdetransaktionen.</span><span class="sxs-lookup"><span data-stu-id="75947-115">If the batch job encounters errors in the dimension setup, it overrides these errors and uses the dimensions of the value entry.</span></span> <span data-ttu-id="75947-116">För andra fel bokför batch-jobbet inte värdetransaktionerna och anger dem vid slutet av rapporten i avsnittet **Transaktioner som hoppats över**.</span><span class="sxs-lookup"><span data-stu-id="75947-116">For other errors, the batch job does not post the value entries and lists them at the end of the report in a section titled, **Skipped Entries**.</span></span> <span data-ttu-id="75947-117">För att bokföra de här transaktionerna måste du först lösa felen.</span><span class="sxs-lookup"><span data-stu-id="75947-117">To post these entries, you must first fix the errors.</span></span> <span data-ttu-id="75947-118">Om en lista över felen ska visas innan batch-jobbet för bokföring ska köras kan rapporten **Bokför lagerkostnad i redovisning**.</span><span class="sxs-lookup"><span data-stu-id="75947-118">To see a list of errors before you run the batch job, you can run the **Post Invt. Cost to G/L - Test** report.</span></span> <span data-ttu-id="75947-119">Alla fel som inträffar under testbokföringen visas i en lista i testrapporten.</span><span class="sxs-lookup"><span data-stu-id="75947-119">This report lists all of the errors that are encountered during a test posting.</span></span> <span data-ttu-id="75947-120">Därefter går det att korrigera felen och köra batch-jobbet för bokföringen av lagerkostnaden utan att transaktioner hoppas över.</span><span class="sxs-lookup"><span data-stu-id="75947-120">You can fix the errors, and then run the inventory cost posting batch job without skipping any entries.</span></span>  

## <a name="automatic-cost-posting"></a><span data-ttu-id="75947-121">Automatisk kostnadsbokföring</span><span class="sxs-lookup"><span data-stu-id="75947-121">Automatic Cost Posting</span></span>  
<span data-ttu-id="75947-122">Om du vill göra så att kostnadsbokföringen till redovisningen körs automatiskt när du bokför en lagertransaktion markerar du kryssrutan **Automatisk kostnadsbokföring** i fönstret **Lagerinställning**.</span><span class="sxs-lookup"><span data-stu-id="75947-122">To set up cost posting to the general ledger to run automatically when you post an inventory transaction, select the **Automatic Cost Posting** check box in the **Inventory Setup** window.</span></span> <span data-ttu-id="75947-123">Bokföringsdatumet för redovisningstransaktionen är detsamma som bokföringsdatumet för artikeltransaktionen.</span><span class="sxs-lookup"><span data-stu-id="75947-123">The posting date of the general ledger entry is the same as the posting date of the item ledger entry.</span></span>  

## <a name="account-types"></a><span data-ttu-id="75947-124">Kontotyper</span><span class="sxs-lookup"><span data-stu-id="75947-124">Account Types</span></span>  
<span data-ttu-id="75947-125">Under avstämning bokförs lagervärden i lagerkontot i balansräkningen.</span><span class="sxs-lookup"><span data-stu-id="75947-125">During reconciliation, inventory values are posted to the inventory account in the balance sheet.</span></span> <span data-ttu-id="75947-126">Samma belopp, men med omvänt tecken, bokförs på det relevanta motkontot.</span><span class="sxs-lookup"><span data-stu-id="75947-126">The same amount, but with the reverse sign, is posted to the relevant balancing account.</span></span> <span data-ttu-id="75947-127">Vanligtvis är motkontot ett resultaträkningkonto.</span><span class="sxs-lookup"><span data-stu-id="75947-127">Usually the balancing account is an income statement account.</span></span> <span data-ttu-id="75947-128">Men när du bokför direkt kostnad som hör till förbrukning eller utflöde är motkontot ett balansräkningskonto.</span><span class="sxs-lookup"><span data-stu-id="75947-128">However, when you post direct cost related to consumption or output, the balancing account is a balance sheet account.</span></span> <span data-ttu-id="75947-129">Typen av artikeltransaktion och värdetransaktionen avgör vilket redovisningskonto att bokföra på.</span><span class="sxs-lookup"><span data-stu-id="75947-129">The type of the item ledger entry and value entry determines which general ledger account to post to.</span></span>  

<span data-ttu-id="75947-130">Transaktionstypen anger vilket redovisningskonto att bokföra på.</span><span class="sxs-lookup"><span data-stu-id="75947-130">The entry type indicates which general ledger account to post to.</span></span> <span data-ttu-id="75947-131">Det bestäms antingen av antalets tecken i artikeltransaktionen eller det värderade antalet i värdetransaktionen, eftersom antalen har alltid samma tecken.</span><span class="sxs-lookup"><span data-stu-id="75947-131">This is determined either by the sign of the quantity on the item ledger entry or the valued quantity on the value entry, since the quantities always have the same sign.</span></span> <span data-ttu-id="75947-132">En försäljningspost med ett positivt antal beskriver till exempel en lagerminskning som orsakas av en försäljning, och en försäljningstransaktion med ett negativt antal beskriver en lagerökning som orsakas av en försäljningsretur.</span><span class="sxs-lookup"><span data-stu-id="75947-132">For example, a sales entry with a positive quantity describes an inventory decrease caused by a sale, and a sales entry with a negative quantity describes an inventory increase caused by a sales return.</span></span>  

### <a name="example"></a><span data-ttu-id="75947-133">Exempel</span><span class="sxs-lookup"><span data-stu-id="75947-133">Example</span></span>  
<span data-ttu-id="75947-134">Följande exempel visar en cykelkedja som tillverkas av inköpta länkar.</span><span class="sxs-lookup"><span data-stu-id="75947-134">The following example shows a bike chain that is manufactured from purchased links.</span></span> <span data-ttu-id="75947-135">I det här exemplet visas hur de olika redovisningskontotyperna används i ett typiskt scenario.</span><span class="sxs-lookup"><span data-stu-id="75947-135">This example shows how the various general ledger account types are used in a typical scenario.</span></span>  

<span data-ttu-id="75947-136">Kryssrutan **Förväntad kost.bokf. i redovisningen** i fönstret **Lagerinställningar** är markerad i och följande inställning har definierats.</span><span class="sxs-lookup"><span data-stu-id="75947-136">The **Expected Cost Posting to G/L** check box in the **Inventory Setup** window is selected, and the following setup is defined.</span></span>  

<span data-ttu-id="75947-137">Följande tabell visar hur länken ställs in på artikelkortet.</span><span class="sxs-lookup"><span data-stu-id="75947-137">The following table shows how the link is set up on the item card.</span></span>  

|<span data-ttu-id="75947-138">Inställningsfält</span><span class="sxs-lookup"><span data-stu-id="75947-138">Setup Field</span></span>|<span data-ttu-id="75947-139">Värde</span><span class="sxs-lookup"><span data-stu-id="75947-139">Value</span></span>|  
|-----------------|-----------|  
|<span data-ttu-id="75947-140">**Värderingsprincip**</span><span class="sxs-lookup"><span data-stu-id="75947-140">**Costing Method**</span></span>|<span data-ttu-id="75947-141">Standard</span><span class="sxs-lookup"><span data-stu-id="75947-141">Standard</span></span>|  
|<span data-ttu-id="75947-142">**Standardkostnad**</span><span class="sxs-lookup"><span data-stu-id="75947-142">**Standard Cost**</span></span>|<span data-ttu-id="75947-143">1,00 SEK</span><span class="sxs-lookup"><span data-stu-id="75947-143">LCY 1.00</span></span>|  
|<span data-ttu-id="75947-144">**Omkostnad**</span><span class="sxs-lookup"><span data-stu-id="75947-144">**Overhead Rate**</span></span>|<span data-ttu-id="75947-145">0,02 SEK</span><span class="sxs-lookup"><span data-stu-id="75947-145">LCY 0.02</span></span>|  

<span data-ttu-id="75947-146">Följande tabell visar hur kedjan ställs in på artikelkortet.</span><span class="sxs-lookup"><span data-stu-id="75947-146">The following table shows how the chain is set up on the item card.</span></span>  

|<span data-ttu-id="75947-147">Inställningsfält</span><span class="sxs-lookup"><span data-stu-id="75947-147">Setup Field</span></span>|<span data-ttu-id="75947-148">Värde</span><span class="sxs-lookup"><span data-stu-id="75947-148">Value</span></span>|  
|-----------------|-----------|  
|<span data-ttu-id="75947-149">**Värderingsprincip**</span><span class="sxs-lookup"><span data-stu-id="75947-149">**Costing Method**</span></span>|<span data-ttu-id="75947-150">Standard</span><span class="sxs-lookup"><span data-stu-id="75947-150">Standard</span></span>|  
|<span data-ttu-id="75947-151">**Standardkostnad**</span><span class="sxs-lookup"><span data-stu-id="75947-151">**Standard Cost**</span></span>|<span data-ttu-id="75947-152">150,00 SEK</span><span class="sxs-lookup"><span data-stu-id="75947-152">LCY 150.00</span></span>|  
|<span data-ttu-id="75947-153">**Omkostnad**</span><span class="sxs-lookup"><span data-stu-id="75947-153">**Overhead Rate**</span></span>|<span data-ttu-id="75947-154">25,00 SEK</span><span class="sxs-lookup"><span data-stu-id="75947-154">LCY 25.00</span></span>|  

<span data-ttu-id="75947-155">Följande tabell visar hur länken produktionsgruppen ställs in på produktionsgruppskortet.</span><span class="sxs-lookup"><span data-stu-id="75947-155">The following table shows how the work center is set up on the work center card.</span></span>  

|<span data-ttu-id="75947-156">Inställningsfält</span><span class="sxs-lookup"><span data-stu-id="75947-156">Setup Field</span></span>|<span data-ttu-id="75947-157">Värde</span><span class="sxs-lookup"><span data-stu-id="75947-157">Value</span></span>|  
|-----------------|-----------|  
|<span data-ttu-id="75947-158">**A-pris senaste inköp**</span><span class="sxs-lookup"><span data-stu-id="75947-158">**Direct Unit Cost**</span></span>|<span data-ttu-id="75947-159">2,00 SEK</span><span class="sxs-lookup"><span data-stu-id="75947-159">LCY 2.00</span></span>|  
|<span data-ttu-id="75947-160">**Omkostnad %**</span><span class="sxs-lookup"><span data-stu-id="75947-160">**Indirect Cost Percentage**</span></span>|<span data-ttu-id="75947-161">10</span><span class="sxs-lookup"><span data-stu-id="75947-161">10</span></span>|  

##### <a name="scenario"></a><span data-ttu-id="75947-162">Scenario</span><span class="sxs-lookup"><span data-stu-id="75947-162">Scenario</span></span>  
1. <span data-ttu-id="75947-163">Användaren köpen 150 länkar och bokför inköpsordern som inlevererad.</span><span class="sxs-lookup"><span data-stu-id="75947-163">The user purchases 150 links and posts the purchase order as received.</span></span> <span data-ttu-id="75947-164">(Inköp)</span><span class="sxs-lookup"><span data-stu-id="75947-164">(Purchase)</span></span>  
2. <span data-ttu-id="75947-165">Användaren bokför inköpsordern som fakturerad.</span><span class="sxs-lookup"><span data-stu-id="75947-165">The user posts the purchase order as invoiced.</span></span> <span data-ttu-id="75947-166">Det skapas ett omkostnadsbelopp på BVA 3,00 som ska fördelas och ett avvikelsebelopp på BVA 18,00.</span><span class="sxs-lookup"><span data-stu-id="75947-166">This creates an overhead amount of LCY 3.00 to be allocated and a variance amount of LCY 18.00.</span></span> <span data-ttu-id="75947-167">(Inköp)</span><span class="sxs-lookup"><span data-stu-id="75947-167">(Purchase)</span></span>  

    1. <span data-ttu-id="75947-168">Interimskontona rensas.</span><span class="sxs-lookup"><span data-stu-id="75947-168">The interim accounts are cleared.</span></span> <span data-ttu-id="75947-169">(Inköp)</span><span class="sxs-lookup"><span data-stu-id="75947-169">(Purchase)</span></span>  
    2. <span data-ttu-id="75947-170">Direkt kostnad bokförs.</span><span class="sxs-lookup"><span data-stu-id="75947-170">The direct cost is posted.</span></span> <span data-ttu-id="75947-171">(Inköp)</span><span class="sxs-lookup"><span data-stu-id="75947-171">(Purchase)</span></span>  
    3. <span data-ttu-id="75947-172">Indirekt kostnad beräknas och bokförs.</span><span class="sxs-lookup"><span data-stu-id="75947-172">The indirect cost is calculated and posted.</span></span> <span data-ttu-id="75947-173">(Inköp)</span><span class="sxs-lookup"><span data-stu-id="75947-173">(Purchase)</span></span>  
    4. <span data-ttu-id="75947-174">Inköpsvariansen beräknas och bokförs (endast för standardkostnadobjekt).</span><span class="sxs-lookup"><span data-stu-id="75947-174">The purchase variance is calculated and posted (only for standard-cost items).</span></span> <span data-ttu-id="75947-175">(Inköp)</span><span class="sxs-lookup"><span data-stu-id="75947-175">(Purchase)</span></span>  
3. <span data-ttu-id="75947-176">Användaren säljer en kedja och bokför försäljningsordern som levererad.</span><span class="sxs-lookup"><span data-stu-id="75947-176">The user sells one chain and posts the sales order as shipped.</span></span> <span data-ttu-id="75947-177">(Försäljning)</span><span class="sxs-lookup"><span data-stu-id="75947-177">(Sale)</span></span>  
4. <span data-ttu-id="75947-178">Användaren bokför försäljningsordern som fakturerad.</span><span class="sxs-lookup"><span data-stu-id="75947-178">The user posts the sales order as invoiced.</span></span> <span data-ttu-id="75947-179">(Försäljning)</span><span class="sxs-lookup"><span data-stu-id="75947-179">(Sale)</span></span>  

    1. <span data-ttu-id="75947-180">Interimskontona rensas.</span><span class="sxs-lookup"><span data-stu-id="75947-180">The interim accounts are cleared.</span></span> <span data-ttu-id="75947-181">(Försäljning)</span><span class="sxs-lookup"><span data-stu-id="75947-181">(Sale)</span></span>  
    2. <span data-ttu-id="75947-182">Kostnaden för sålda varor (KSV) bokförs.</span><span class="sxs-lookup"><span data-stu-id="75947-182">Cost of goods sold (COGS) is posted.</span></span> <span data-ttu-id="75947-183">(Försäljning)</span><span class="sxs-lookup"><span data-stu-id="75947-183">(Sale)</span></span>  

        <span data-ttu-id="75947-184">![Resultatet av försäljningsbokföring till G&#47;L-konton](media/design_details_inventory_costing_3_gl_posting_sales.png "design_details_inventory_costing_3_GL_posting_sales")</span><span class="sxs-lookup"><span data-stu-id="75947-184">![Results of sale posting to G&#47;L accounts](media/design_details_inventory_costing_3_gl_posting_sales.png "design_details_inventory_costing_3_GL_posting_sales")</span></span>  
5. <span data-ttu-id="75947-185">Användaren bokför förbrukning av 150 länkar, som är antalet länkar som används för att producera en kedja.</span><span class="sxs-lookup"><span data-stu-id="75947-185">The user posts consumption of 150 links, which is the number of links used to produce one chain.</span></span> <span data-ttu-id="75947-186">(Förbrukning, material)</span><span class="sxs-lookup"><span data-stu-id="75947-186">(Consumption, Material)</span></span>  

    <span data-ttu-id="75947-187">![Resultatet av materialbokföring till G&#47;L-konton](media/design_details_inventory_costing_3_gl_posting_material.png "design_details_inventory_costing_3_GL_posting_material")</span><span class="sxs-lookup"><span data-stu-id="75947-187">![Results of material posting to G&#47;L accounts](media/design_details_inventory_costing_3_gl_posting_material.png "design_details_inventory_costing_3_GL_posting_material")</span></span>  
6. <span data-ttu-id="75947-188">Produktionsgruppen använde 60 minuter för att producera kedjan.</span><span class="sxs-lookup"><span data-stu-id="75947-188">The work center used 60 minutes to produce the chain.</span></span> <span data-ttu-id="75947-189">Användaren bokför konverteringskostnaden.</span><span class="sxs-lookup"><span data-stu-id="75947-189">The user posts the conversion cost.</span></span> <span data-ttu-id="75947-190">(Förbrukning, Kapacitet)</span><span class="sxs-lookup"><span data-stu-id="75947-190">(Consumption, Capacity)</span></span>  

    1. <span data-ttu-id="75947-191">Direkta kostnader bokförs.</span><span class="sxs-lookup"><span data-stu-id="75947-191">The direct costs are posted.</span></span> <span data-ttu-id="75947-192">(Förbrukning, Kapacitet)</span><span class="sxs-lookup"><span data-stu-id="75947-192">(Consumption, Capacity)</span></span>  
    2. <span data-ttu-id="75947-193">Indirekta kostnader beräknas och bokförs.</span><span class="sxs-lookup"><span data-stu-id="75947-193">The indirect costs are calculated and posted.</span></span> <span data-ttu-id="75947-194">(Förbrukning, Kapacitet)</span><span class="sxs-lookup"><span data-stu-id="75947-194">(Consumption, Capacity)</span></span>  

        <span data-ttu-id="75947-195">![Resultatet av kapacitetsbokföring till G&#47;L-konton](media/design_details_inventory_costing_3_gl_posting_capacity.png "design_details_inventory_costing_3_GL_posting_capacity")</span><span class="sxs-lookup"><span data-stu-id="75947-195">![Results of capacity posting to G&#47;L accounts](media/design_details_inventory_costing_3_gl_posting_capacity.png "design_details_inventory_costing_3_GL_posting_capacity")</span></span>  
7. <span data-ttu-id="75947-196">Användaren bokför förväntade kostnaden för en kedja.</span><span class="sxs-lookup"><span data-stu-id="75947-196">The user posts the expected cost of one chain.</span></span> <span data-ttu-id="75947-197">(Utflöde)</span><span class="sxs-lookup"><span data-stu-id="75947-197">(Output)</span></span>  
8. <span data-ttu-id="75947-198">Användaren avslutar produktionsordern och kör batch-jobbet **Justera kost. - artikel trans**.</span><span class="sxs-lookup"><span data-stu-id="75947-198">The user finishes the production order and runs the **Adjust Cost - Item Entries** batch job.</span></span> <span data-ttu-id="75947-199">(Utflöde)</span><span class="sxs-lookup"><span data-stu-id="75947-199">(Output)</span></span>  

    1. <span data-ttu-id="75947-200">Interimskontona rensas.</span><span class="sxs-lookup"><span data-stu-id="75947-200">The interim accounts are cleared.</span></span> <span data-ttu-id="75947-201">(Utflöde)</span><span class="sxs-lookup"><span data-stu-id="75947-201">(Output)</span></span>  
    2. <span data-ttu-id="75947-202">Den direkta kostnaden överförs från PIA-kontot till lagerkontot.</span><span class="sxs-lookup"><span data-stu-id="75947-202">The direct cost is transferred from the WIP account to the inventory account.</span></span> <span data-ttu-id="75947-203">(Utflöde)</span><span class="sxs-lookup"><span data-stu-id="75947-203">(Output)</span></span>  
    3. <span data-ttu-id="75947-204">Den indirekta kostnaden (omkostnader) överförs från kontot för indirekt kostnad till lagerkontot.</span><span class="sxs-lookup"><span data-stu-id="75947-204">The indirect cost (overhead) is transferred from the indirect cost account to the inventory account.</span></span> <span data-ttu-id="75947-205">(Utflöde)</span><span class="sxs-lookup"><span data-stu-id="75947-205">(Output)</span></span>  
    4. <span data-ttu-id="75947-206">Det resulterar i ett avvikelsebelopp på BVA 157,00.</span><span class="sxs-lookup"><span data-stu-id="75947-206">This results in a variance amount of LCY 157.00.</span></span> <span data-ttu-id="75947-207">Varianser beräknas endast för standardkostnadobjekt.</span><span class="sxs-lookup"><span data-stu-id="75947-207">Variances are only calculated for standard-cost items.</span></span> <span data-ttu-id="75947-208">(Utflöde)</span><span class="sxs-lookup"><span data-stu-id="75947-208">(Output)</span></span>  

        <span data-ttu-id="75947-209">![Resultatet av utflödesbokföring till G&#47;L-konton](media/design_details_inventory_costing_3_gl_posting_output.png "design_details_inventory_costing_3_GL_posting_output")</span><span class="sxs-lookup"><span data-stu-id="75947-209">![Results of output posting to G&#47;L accounts](media/design_details_inventory_costing_3_gl_posting_output.png "design_details_inventory_costing_3_GL_posting_output")</span></span>  

        > [!NOTE]  
        >  <span data-ttu-id="75947-210">För enkelhets skull visas bara ett varianskonto.</span><span class="sxs-lookup"><span data-stu-id="75947-210">For the sake of simplicity, only one variance account is shown.</span></span> <span data-ttu-id="75947-211">I verkligheten finns fem olika konton:</span><span class="sxs-lookup"><span data-stu-id="75947-211">In reality, five different accounts exist:</span></span>  
        >   
        >  * <span data-ttu-id="75947-212">Materialvarians</span><span class="sxs-lookup"><span data-stu-id="75947-212">Material Variance</span></span>  
        >  * <span data-ttu-id="75947-213">Kapacitetsvarians</span><span class="sxs-lookup"><span data-stu-id="75947-213">Capacity Variance</span></span>  
        >  * <span data-ttu-id="75947-214">Kapacitetsomkostnadsvarians</span><span class="sxs-lookup"><span data-stu-id="75947-214">Capacity Overhead Variance</span></span>  
        >  * <span data-ttu-id="75947-215">Legotillverkning varians</span><span class="sxs-lookup"><span data-stu-id="75947-215">Subcontracting Variance</span></span>  
        >  * <span data-ttu-id="75947-216">Produktionsomkostnadsvarians</span><span class="sxs-lookup"><span data-stu-id="75947-216">Manufacturing Overhead Variance</span></span>  

9. <span data-ttu-id="75947-217">Användaren omvärderar kedjan från BVA 150,00 till BVA 140,00.</span><span class="sxs-lookup"><span data-stu-id="75947-217">The user revalues the chain from LCY 150.00 to LCY 140.00.</span></span> <span data-ttu-id="75947-218">(Justering/Omvärdering/Avrundning/Överföring)</span><span class="sxs-lookup"><span data-stu-id="75947-218">(Adjustment/Revaluation/Rounding/Transfer)</span></span>  

    <span data-ttu-id="75947-219">![Resultatet av justeringsbokföring till G&#47;L-konton](media/design_details_inventory_costing_3_gl_posting_adjustment.png "design_details_inventory_costing_3_GL_posting_adjustment")</span><span class="sxs-lookup"><span data-stu-id="75947-219">![Results of adjustment posting to G&#47;L accounts](media/design_details_inventory_costing_3_gl_posting_adjustment.png "design_details_inventory_costing_3_GL_posting_adjustment")</span></span>  

<span data-ttu-id="75947-220">För mer information om sambandet mellan kontotyperna och de olika typerna av värden, se [Designdetaljer: Konton i redovisningen](design-details-accounts-in-the-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="75947-220">For more information about the relationship between the account types and the different types of value entries, see [Design Details: Accounts in the General Ledger](design-details-accounts-in-the-general-ledger.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="75947-221">Se även</span><span class="sxs-lookup"><span data-stu-id="75947-221">See Also</span></span>  
<span data-ttu-id="75947-222">[Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md) </span><span class="sxs-lookup"><span data-stu-id="75947-222">[Design Details: Inventory Costing](design-details-inventory-costing.md) </span></span>  
<span data-ttu-id="75947-223">[Designdetaljer: Bokföring av förväntad kostnad](design-details-expected-cost-posting.md) </span><span class="sxs-lookup"><span data-stu-id="75947-223">[Design Details: Expected Cost Posting](design-details-expected-cost-posting.md) </span></span>  
<span data-ttu-id="75947-224">[Designdetaljer: kostnadsjustering](design-details-cost-adjustment.md)
[Hantera lagerkostnader](finance-manage-inventory-costs.md)</span><span class="sxs-lookup"><span data-stu-id="75947-224">[Design Details: Cost Adjustment](design-details-cost-adjustment.md)
[Managing Inventory Costs](finance-manage-inventory-costs.md)</span></span>  
[<span data-ttu-id="75947-225">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="75947-225">Finance</span></span>](finance.md)  
<span data-ttu-id="75947-226">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="75947-226">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
