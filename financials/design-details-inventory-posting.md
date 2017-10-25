---
title: "Designdetaljer - Lagerbokföring | Microsoft Docs"
description: "Varje lagertransaktion, t.ex en inköpsinleverans eller en utleverans, bokför två transaktioner av olika typer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9bc177d45efa1e6e772ed70cc66de393e6250def
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-inventory-posting"></a><span data-ttu-id="2ccd6-103">Designdetaljer: Lagerbokföring</span><span class="sxs-lookup"><span data-stu-id="2ccd6-103">Design Details: Inventory Posting</span></span>
<span data-ttu-id="2ccd6-104">Varje lagertransaktion, t.ex en inköpsinleverans eller en utleverans, bokför två transaktioner av olika typer.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-104">Each inventory transaction, such as a purchase receipt or a sales shipment, posts two entries of different types.</span></span>  

|<span data-ttu-id="2ccd6-105">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="2ccd6-105">Entry type</span></span>|<span data-ttu-id="2ccd6-106">Description</span><span class="sxs-lookup"><span data-stu-id="2ccd6-106">Description</span></span>|  
|----------------|---------------------------------------|  
|<span data-ttu-id="2ccd6-107">Antal</span><span class="sxs-lookup"><span data-stu-id="2ccd6-107">Quantity</span></span>|<span data-ttu-id="2ccd6-108">Återspeglar förändringen av antalet i lager.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-108">Reflects the change of quantity in inventory.</span></span> <span data-ttu-id="2ccd6-109">Informationen lagras som artikeltransaktioner.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-109">This information is stored in item ledger entries.</span></span><br /><br /> <span data-ttu-id="2ccd6-110">Tillsammans med artikelkopplingstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-110">Accompanied by item application entries.</span></span>|  
|<span data-ttu-id="2ccd6-111">Värde</span><span class="sxs-lookup"><span data-stu-id="2ccd6-111">Value</span></span>|<span data-ttu-id="2ccd6-112">Återspeglar förändringen av lagervärdet.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-112">Reflects the change of inventory value.</span></span> <span data-ttu-id="2ccd6-113">Informationen lagras som värdetransaktioner.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-113">This information is stored in value entries.</span></span><br /><br /> <span data-ttu-id="2ccd6-114">Det kan finnas en eller flera värdetransaktioner för varje artikeltransaktion eller kapacitetstransaktion.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-114">One or more value entries can exist for each item ledger entry or capacity ledger entry.</span></span><br /><br /> <span data-ttu-id="2ccd6-115">Se [Designdetaljer: Bokföring av produktionsorder](design-details-production-order-posting.md) för information om kapacitetvärdetransaktioner som rör användningen av produktions- eller monteringsresurser.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-115">For information about capacity value entries related to the use of production or assembly resources, see [Design Details: Production Order Posting](design-details-production-order-posting.md).</span></span>|  

 <span data-ttu-id="2ccd6-116">I relation till antalsbokföringar finns artikelkopplingstransaktioner för att koppla lagerökning till lagerminskning.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-116">In relation to quantity postings, item application entries exist to link inventory increase with inventory decrease.</span></span> <span data-ttu-id="2ccd6-117">Det gör det möjligt för värderingsmotorn att flytta kostnader framåt från ökningar till de relaterade minskningarna och vice versa.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-117">This enables the costing engine to forward costs from increases to the related decreases and vice versa.</span></span> <span data-ttu-id="2ccd6-118">Mer information finns i [Designdetaljer: Artikelspårning](design-details-item-application.md).</span><span class="sxs-lookup"><span data-stu-id="2ccd6-118">For more information, see [Design Details: Item Application](design-details-item-application.md).</span></span>  

 <span data-ttu-id="2ccd6-119">Artikeltransaktioner, värdetransaktioner och artikelkopplingstransaktioner skapas som ett resultat av att bokföra en artikeljournalrad, antingen indirekt genom att bokföra en orderrad eller direkt i fönstret Artikeljournal.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-119">Item ledger entries, value entries, and item application entries are created as a result of posting an item journal line, either indirectly by posting an order line or directly in the Item Journal window.</span></span>  

 <span data-ttu-id="2ccd6-120">Med regelbundna intervall bokförs värdetransaktioner som skapas i inventeringen i redovisningen för att stämma av de två redovisningarna för ekonomisk kontroll.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-120">At regular intervals, value entries that are created in the inventory ledger are posted to the general ledger to reconcile the two ledgers for financial control reasons.</span></span> <span data-ttu-id="2ccd6-121">Mer information finns i [detaljer: avstämning med redovisningen](design-details-reconciliation-with-the-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="2ccd6-121">For more information, see [Design Details: Reconciliation with the General Ledger](design-details-reconciliation-with-the-general-ledger.md).</span></span>  

 <span data-ttu-id="2ccd6-122">![Transaktionsflöde mellan lager och redovisning & #47; L](media/design_details_inventory_costing_1_entry_flow.png "design_details_inventory_costing_1_entry_flow")</span><span class="sxs-lookup"><span data-stu-id="2ccd6-122">![Entry flow between inventory and G&#47;L](media/design_details_inventory_costing_1_entry_flow.png "design_details_inventory_costing_1_entry_flow")</span></span>  

## <a name="example"></a><span data-ttu-id="2ccd6-123">Exempel</span><span class="sxs-lookup"><span data-stu-id="2ccd6-123">Example</span></span>  
 <span data-ttu-id="2ccd6-124">Följande exempel visar hur artikeltransaktioner, värdetransaktioner och artikelkopplingstransaktioner skapas i redovisningstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-124">The following example shows how item ledger entries, value entries, and item application entries result in general ledger entries.</span></span>  

 <span data-ttu-id="2ccd6-125">Du bokför en inköpsorder som har inlevererats och fakturerats för 10 artiklar med en direkt enhetskostnad på BVA 7 och en omkostnad på BVA 1.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-125">You post a purchase order as received and invoiced for 10 items with a direct unit cost of LCY 7 and an overhead rate of LCY 1.</span></span> <span data-ttu-id="2ccd6-126">Bokföringsdatumet är 20-01-01.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-126">The posting date is 01-01-20.</span></span> <span data-ttu-id="2ccd6-127">Följande transaktioner upprättas.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-127">The following entries are created.</span></span>  

 <span data-ttu-id="2ccd6-128">**Artikeltransaktioner**</span><span class="sxs-lookup"><span data-stu-id="2ccd6-128">**Item Ledger Entries**</span></span>  

|<span data-ttu-id="2ccd6-129">Bokföringsdatum</span><span class="sxs-lookup"><span data-stu-id="2ccd6-129">Posting Date</span></span>|<span data-ttu-id="2ccd6-130">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="2ccd6-130">Entry Type</span></span>|<span data-ttu-id="2ccd6-131">Kost.belopp (aktuellt)</span><span class="sxs-lookup"><span data-stu-id="2ccd6-131">Cost Amount (Actual)</span></span>|<span data-ttu-id="2ccd6-132">Antal</span><span class="sxs-lookup"><span data-stu-id="2ccd6-132">Quantity</span></span>|<span data-ttu-id="2ccd6-133">Löpnr</span><span class="sxs-lookup"><span data-stu-id="2ccd6-133">Entry No.</span></span>|  
|------------------|----------------|----------------------------|--------------|---------------|  
|<span data-ttu-id="2ccd6-134">01-01-20</span><span class="sxs-lookup"><span data-stu-id="2ccd6-134">01-01-20</span></span>|<span data-ttu-id="2ccd6-135">Inköp</span><span class="sxs-lookup"><span data-stu-id="2ccd6-135">Purchase</span></span>|<span data-ttu-id="2ccd6-136">80.00</span><span class="sxs-lookup"><span data-stu-id="2ccd6-136">80.00</span></span>|<span data-ttu-id="2ccd6-137">10</span><span class="sxs-lookup"><span data-stu-id="2ccd6-137">10</span></span>|<span data-ttu-id="2ccd6-138">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-138">1</span></span>|  

 <span data-ttu-id="2ccd6-139">**Värdetransaktioner**</span><span class="sxs-lookup"><span data-stu-id="2ccd6-139">**Value Entries**</span></span>  

|<span data-ttu-id="2ccd6-140">Bokföringsdatum</span><span class="sxs-lookup"><span data-stu-id="2ccd6-140">Posting Date</span></span>|<span data-ttu-id="2ccd6-141">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="2ccd6-141">Entry Type</span></span>|<span data-ttu-id="2ccd6-142">Kost.belopp (aktuellt)</span><span class="sxs-lookup"><span data-stu-id="2ccd6-142">Cost Amount (Actual)</span></span>|<span data-ttu-id="2ccd6-143">Artikeltrans.löpnr</span><span class="sxs-lookup"><span data-stu-id="2ccd6-143">Item Ledger Entry No.</span></span>|<span data-ttu-id="2ccd6-144">Löpnr</span><span class="sxs-lookup"><span data-stu-id="2ccd6-144">Entry No.</span></span>|  
|------------------|----------------|----------------------------|---------------------------|---------------|  
|<span data-ttu-id="2ccd6-145">01-01-20</span><span class="sxs-lookup"><span data-stu-id="2ccd6-145">01-01-20</span></span>|<span data-ttu-id="2ccd6-146">Inköpskostnad</span><span class="sxs-lookup"><span data-stu-id="2ccd6-146">Direct Cost</span></span>|<span data-ttu-id="2ccd6-147">70,00</span><span class="sxs-lookup"><span data-stu-id="2ccd6-147">70.00</span></span>|<span data-ttu-id="2ccd6-148">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-148">1</span></span>|<span data-ttu-id="2ccd6-149">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-149">1</span></span>|  
|<span data-ttu-id="2ccd6-150">01-01-20</span><span class="sxs-lookup"><span data-stu-id="2ccd6-150">01-01-20</span></span>|<span data-ttu-id="2ccd6-151">Indirekt kostnad</span><span class="sxs-lookup"><span data-stu-id="2ccd6-151">Indirect Cost</span></span>|<span data-ttu-id="2ccd6-152">10,00</span><span class="sxs-lookup"><span data-stu-id="2ccd6-152">10.00</span></span>|<span data-ttu-id="2ccd6-153">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-153">1</span></span>|<span data-ttu-id="2ccd6-154">2</span><span class="sxs-lookup"><span data-stu-id="2ccd6-154">2</span></span>|  

 <span data-ttu-id="2ccd6-155">**Kopplingstransaktioner för artikel**</span><span class="sxs-lookup"><span data-stu-id="2ccd6-155">**Item Application Entries**</span></span>  

|<span data-ttu-id="2ccd6-156">Löpnr</span><span class="sxs-lookup"><span data-stu-id="2ccd6-156">Entry No.</span></span>|<span data-ttu-id="2ccd6-157">Artikeltrans.löpnr</span><span class="sxs-lookup"><span data-stu-id="2ccd6-157">Item Ledger Entry No.</span></span>|<span data-ttu-id="2ccd6-158">Ankommande artikeltrans.nr</span><span class="sxs-lookup"><span data-stu-id="2ccd6-158">Inbound Item Entry No.</span></span>|<span data-ttu-id="2ccd6-159">Avgående artikeltrans.nr</span><span class="sxs-lookup"><span data-stu-id="2ccd6-159">Outbound Item Entry No.</span></span>|<span data-ttu-id="2ccd6-160">Antal</span><span class="sxs-lookup"><span data-stu-id="2ccd6-160">Quantity</span></span>|  
|---------------|---------------------------|----------------------------|-----------------------------|--------------|  
|<span data-ttu-id="2ccd6-161">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-161">1</span></span>|<span data-ttu-id="2ccd6-162">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-162">1</span></span>|<span data-ttu-id="2ccd6-163">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-163">1</span></span>|<span data-ttu-id="2ccd6-164">0</span><span class="sxs-lookup"><span data-stu-id="2ccd6-164">0</span></span>|<span data-ttu-id="2ccd6-165">10</span><span class="sxs-lookup"><span data-stu-id="2ccd6-165">10</span></span>|  

 <span data-ttu-id="2ccd6-166">Nu bokför du en försäljning på 10 enheter av artikeln med ett bokföringsdatum på 01-15-20.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-166">Next, you post a sale of 10 units of the item with a posting date of 01-15-20.</span></span>  

 <span data-ttu-id="2ccd6-167">**Artikeltransaktioner**</span><span class="sxs-lookup"><span data-stu-id="2ccd6-167">**Item Ledger Entries**</span></span>  

|<span data-ttu-id="2ccd6-168">Bokföringsdatum</span><span class="sxs-lookup"><span data-stu-id="2ccd6-168">Posting Date</span></span>|<span data-ttu-id="2ccd6-169">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="2ccd6-169">Entry Type</span></span>|<span data-ttu-id="2ccd6-170">Kost.belopp (aktuellt)</span><span class="sxs-lookup"><span data-stu-id="2ccd6-170">Cost Amount (Actual)</span></span>||<span data-ttu-id="2ccd6-171">Antal</span><span class="sxs-lookup"><span data-stu-id="2ccd6-171">Quantity</span></span>|<span data-ttu-id="2ccd6-172">Löpnr</span><span class="sxs-lookup"><span data-stu-id="2ccd6-172">Entry No.</span></span>|  
|------------------|----------------|----------------------------|-|--------------|---------------|  
|<span data-ttu-id="2ccd6-173">01-15-20</span><span class="sxs-lookup"><span data-stu-id="2ccd6-173">01-15-20</span></span>|<span data-ttu-id="2ccd6-174">Försäljning</span><span class="sxs-lookup"><span data-stu-id="2ccd6-174">Sale</span></span>|<span data-ttu-id="2ccd6-175">-80.00</span><span class="sxs-lookup"><span data-stu-id="2ccd6-175">-80.00</span></span>||<span data-ttu-id="2ccd6-176">-10</span><span class="sxs-lookup"><span data-stu-id="2ccd6-176">-10</span></span>|<span data-ttu-id="2ccd6-177">2</span><span class="sxs-lookup"><span data-stu-id="2ccd6-177">2</span></span>|  

 <span data-ttu-id="2ccd6-178">**Värdetransaktioner**</span><span class="sxs-lookup"><span data-stu-id="2ccd6-178">**Value Entries**</span></span>  

|<span data-ttu-id="2ccd6-179">Bokföringsdatum</span><span class="sxs-lookup"><span data-stu-id="2ccd6-179">Posting Date</span></span>|<span data-ttu-id="2ccd6-180">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="2ccd6-180">Entry Type</span></span>|<span data-ttu-id="2ccd6-181">Kost.belopp (aktuellt)</span><span class="sxs-lookup"><span data-stu-id="2ccd6-181">Cost Amount (Actual)</span></span>|<span data-ttu-id="2ccd6-182">Artikeltrans.löpnr</span><span class="sxs-lookup"><span data-stu-id="2ccd6-182">Item Ledger Entry No.</span></span>|<span data-ttu-id="2ccd6-183">Löpnr</span><span class="sxs-lookup"><span data-stu-id="2ccd6-183">Entry No.</span></span>|  
|------------------|----------------|----------------------------|---------------------------|---------------|  
|<span data-ttu-id="2ccd6-184">01-15-20</span><span class="sxs-lookup"><span data-stu-id="2ccd6-184">01-15-20</span></span>|<span data-ttu-id="2ccd6-185">Inköpskostnad</span><span class="sxs-lookup"><span data-stu-id="2ccd6-185">Direct Cost</span></span>|<span data-ttu-id="2ccd6-186">-80.00</span><span class="sxs-lookup"><span data-stu-id="2ccd6-186">-80.00</span></span>|<span data-ttu-id="2ccd6-187">2</span><span class="sxs-lookup"><span data-stu-id="2ccd6-187">2</span></span>|<span data-ttu-id="2ccd6-188">3</span><span class="sxs-lookup"><span data-stu-id="2ccd6-188">3</span></span>|  

 <span data-ttu-id="2ccd6-189">**Kopplingstransaktioner för artikel**</span><span class="sxs-lookup"><span data-stu-id="2ccd6-189">**Item Application Entries**</span></span>  

|<span data-ttu-id="2ccd6-190">Löpnr</span><span class="sxs-lookup"><span data-stu-id="2ccd6-190">Entry No.</span></span>|<span data-ttu-id="2ccd6-191">Artikeltrans.löpnr</span><span class="sxs-lookup"><span data-stu-id="2ccd6-191">Item Ledger Entry No.</span></span>|<span data-ttu-id="2ccd6-192">Internt artikeltrans.nr</span><span class="sxs-lookup"><span data-stu-id="2ccd6-192">Inbound Item Entry No.</span></span>|<span data-ttu-id="2ccd6-193">Externt artikeltrans.nr</span><span class="sxs-lookup"><span data-stu-id="2ccd6-193">Outbound Item Entry No.</span></span>|<span data-ttu-id="2ccd6-194">Antal</span><span class="sxs-lookup"><span data-stu-id="2ccd6-194">Quantity</span></span>|  
|---------------|---------------------------|----------------------------|-----------------------------|--------------|  
|<span data-ttu-id="2ccd6-195">2</span><span class="sxs-lookup"><span data-stu-id="2ccd6-195">2</span></span>|<span data-ttu-id="2ccd6-196">2</span><span class="sxs-lookup"><span data-stu-id="2ccd6-196">2</span></span>|<span data-ttu-id="2ccd6-197">0</span><span class="sxs-lookup"><span data-stu-id="2ccd6-197">1</span></span>|<span data-ttu-id="2ccd6-198">2</span><span class="sxs-lookup"><span data-stu-id="2ccd6-198">2</span></span>|<span data-ttu-id="2ccd6-199">-10</span><span class="sxs-lookup"><span data-stu-id="2ccd6-199">-10</span></span>|  

 <span data-ttu-id="2ccd6-200">Vid slutet av bokföringsperioden kör du batchjobbet **Bokför lagerkostnad i redov** för att stämma av de här lagertransaktionerna med redovisningen.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-200">At the end of the accounting period, you run the **Post Inventory Cost to G/L** batch job to reconcile these inventory transactions with the general ledger.</span></span>  

 <span data-ttu-id="2ccd6-201">Mer information finns i [Desigdetaljer: konton i redovisningen](design-details-accounts-in-the-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="2ccd6-201">For more information, see [Design Details: Accounts in the General Ledger](design-details-accounts-in-the-general-ledger.md).</span></span>  

 <span data-ttu-id="2ccd6-202">Följande tabeller visar resultatet av avstämningen av lagertransaktionerna i det här exemplet med redovisningen.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-202">The following tables show the result of reconciling the inventory transactions in this example with the general ledger.</span></span>  

 <span data-ttu-id="2ccd6-203">**Värdetransaktioner**</span><span class="sxs-lookup"><span data-stu-id="2ccd6-203">**Value Entries**</span></span>  

|<span data-ttu-id="2ccd6-204">Bokföringsdatum</span><span class="sxs-lookup"><span data-stu-id="2ccd6-204">Posting Date</span></span>|<span data-ttu-id="2ccd6-205">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="2ccd6-205">Entry Type</span></span>|<span data-ttu-id="2ccd6-206">Kost.belopp (aktuellt)</span><span class="sxs-lookup"><span data-stu-id="2ccd6-206">Cost Amount (Actual)</span></span>|<span data-ttu-id="2ccd6-207">Kostnad bokförd i redov.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-207">Cost Posted to G/L</span></span>|<span data-ttu-id="2ccd6-208">Artikeltrans.löpnr</span><span class="sxs-lookup"><span data-stu-id="2ccd6-208">Item Ledger Entry No.</span></span>|<span data-ttu-id="2ccd6-209">Löpnr</span><span class="sxs-lookup"><span data-stu-id="2ccd6-209">Entry No.</span></span>|  
|------------------|----------------|----------------------------|-------------------------|---------------------------|---------------|  
|<span data-ttu-id="2ccd6-210">01-01-20</span><span class="sxs-lookup"><span data-stu-id="2ccd6-210">01-01-20</span></span>|<span data-ttu-id="2ccd6-211">Inköpskostnad</span><span class="sxs-lookup"><span data-stu-id="2ccd6-211">Direct Cost</span></span>|<span data-ttu-id="2ccd6-212">70,00</span><span class="sxs-lookup"><span data-stu-id="2ccd6-212">70.00</span></span>|<span data-ttu-id="2ccd6-213">70,00</span><span class="sxs-lookup"><span data-stu-id="2ccd6-213">70.00</span></span>|<span data-ttu-id="2ccd6-214">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-214">1</span></span>|<span data-ttu-id="2ccd6-215">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-215">1</span></span>|  
|<span data-ttu-id="2ccd6-216">01-01-20</span><span class="sxs-lookup"><span data-stu-id="2ccd6-216">01-01-20</span></span>|<span data-ttu-id="2ccd6-217">Indirekt kostnad</span><span class="sxs-lookup"><span data-stu-id="2ccd6-217">Indirect Cost</span></span>|<span data-ttu-id="2ccd6-218">10,00</span><span class="sxs-lookup"><span data-stu-id="2ccd6-218">10.00</span></span>|<span data-ttu-id="2ccd6-219">10,00</span><span class="sxs-lookup"><span data-stu-id="2ccd6-219">10.00</span></span>|<span data-ttu-id="2ccd6-220">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-220">1</span></span>|<span data-ttu-id="2ccd6-221">2</span><span class="sxs-lookup"><span data-stu-id="2ccd6-221">2</span></span>|  
|<span data-ttu-id="2ccd6-222">01-15-20</span><span class="sxs-lookup"><span data-stu-id="2ccd6-222">01-15-20</span></span>|<span data-ttu-id="2ccd6-223">Inköpskostnad</span><span class="sxs-lookup"><span data-stu-id="2ccd6-223">Direct Cost</span></span>|<span data-ttu-id="2ccd6-224">-80.00</span><span class="sxs-lookup"><span data-stu-id="2ccd6-224">-80.00</span></span>|<span data-ttu-id="2ccd6-225">-80.00</span><span class="sxs-lookup"><span data-stu-id="2ccd6-225">-80.00</span></span>|<span data-ttu-id="2ccd6-226">2</span><span class="sxs-lookup"><span data-stu-id="2ccd6-226">2</span></span>|<span data-ttu-id="2ccd6-227">3</span><span class="sxs-lookup"><span data-stu-id="2ccd6-227">3</span></span>|  

 <span data-ttu-id="2ccd6-228">**Redovisningstransaktioner**</span><span class="sxs-lookup"><span data-stu-id="2ccd6-228">**General Ledger Entries**</span></span>  

|<span data-ttu-id="2ccd6-229">Bokföringsdatum</span><span class="sxs-lookup"><span data-stu-id="2ccd6-229">Posting Date</span></span>|<span data-ttu-id="2ccd6-230">Redovisningskonto</span><span class="sxs-lookup"><span data-stu-id="2ccd6-230">G/L Account</span></span>|<span data-ttu-id="2ccd6-231">Kontonr. (En-US-demo)</span><span class="sxs-lookup"><span data-stu-id="2ccd6-231">Account No. (En-US Demo)</span></span>||<span data-ttu-id="2ccd6-232">Belopp</span><span class="sxs-lookup"><span data-stu-id="2ccd6-232">Amount</span></span>|<span data-ttu-id="2ccd6-233">Löpnr</span><span class="sxs-lookup"><span data-stu-id="2ccd6-233">Entry No.</span></span>|  
|------------------|------------------|---------------------------------|-|------------|---------------|  
|<span data-ttu-id="2ccd6-234">01-01-20</span><span class="sxs-lookup"><span data-stu-id="2ccd6-234">01-01-20</span></span>|<span data-ttu-id="2ccd6-235">[Lagerkonto]</span><span class="sxs-lookup"><span data-stu-id="2ccd6-235">[Inventory Account]</span></span>|<span data-ttu-id="2ccd6-236">2130</span><span class="sxs-lookup"><span data-stu-id="2ccd6-236">2130</span></span>||<span data-ttu-id="2ccd6-237">70,00</span><span class="sxs-lookup"><span data-stu-id="2ccd6-237">70.00</span></span>|<span data-ttu-id="2ccd6-238">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-238">1</span></span>|  
|<span data-ttu-id="2ccd6-239">01-01-20</span><span class="sxs-lookup"><span data-stu-id="2ccd6-239">01-01-20</span></span>|<span data-ttu-id="2ccd6-240">[Direkt kostnad kopplad - konto]</span><span class="sxs-lookup"><span data-stu-id="2ccd6-240">[Direct Cost Applied Account]</span></span>|<span data-ttu-id="2ccd6-241">7291</span><span class="sxs-lookup"><span data-stu-id="2ccd6-241">7291</span></span>||<span data-ttu-id="2ccd6-242">-70.00</span><span class="sxs-lookup"><span data-stu-id="2ccd6-242">-70.00</span></span>|<span data-ttu-id="2ccd6-243">2</span><span class="sxs-lookup"><span data-stu-id="2ccd6-243">2</span></span>|  
|<span data-ttu-id="2ccd6-244">01-01-20</span><span class="sxs-lookup"><span data-stu-id="2ccd6-244">01-01-20</span></span>|<span data-ttu-id="2ccd6-245">[Lagerkonto]</span><span class="sxs-lookup"><span data-stu-id="2ccd6-245">[Inventory Account]</span></span>|<span data-ttu-id="2ccd6-246">2130</span><span class="sxs-lookup"><span data-stu-id="2ccd6-246">2130</span></span>||<span data-ttu-id="2ccd6-247">10,00</span><span class="sxs-lookup"><span data-stu-id="2ccd6-247">10.00</span></span>|<span data-ttu-id="2ccd6-248">3</span><span class="sxs-lookup"><span data-stu-id="2ccd6-248">3</span></span>|  
|<span data-ttu-id="2ccd6-249">07.01.01</span><span class="sxs-lookup"><span data-stu-id="2ccd6-249">01-01-07</span></span>|<span data-ttu-id="2ccd6-250">[Omkostnader kopplade, konto]</span><span class="sxs-lookup"><span data-stu-id="2ccd6-250">[Overhead Applied Account]</span></span>|<span data-ttu-id="2ccd6-251">7292</span><span class="sxs-lookup"><span data-stu-id="2ccd6-251">7292</span></span>||<span data-ttu-id="2ccd6-252">-10.00</span><span class="sxs-lookup"><span data-stu-id="2ccd6-252">-10.00</span></span>|<span data-ttu-id="2ccd6-253">4</span><span class="sxs-lookup"><span data-stu-id="2ccd6-253">4</span></span>|  
|<span data-ttu-id="2ccd6-254">01-15-20</span><span class="sxs-lookup"><span data-stu-id="2ccd6-254">01-15-20</span></span>|<span data-ttu-id="2ccd6-255">[Lagerkonto]</span><span class="sxs-lookup"><span data-stu-id="2ccd6-255">[Inventory Account]</span></span>|<span data-ttu-id="2ccd6-256">2130</span><span class="sxs-lookup"><span data-stu-id="2ccd6-256">2130</span></span>||<span data-ttu-id="2ccd6-257">-80.00</span><span class="sxs-lookup"><span data-stu-id="2ccd6-257">-80.00</span></span>|<span data-ttu-id="2ccd6-258">5</span><span class="sxs-lookup"><span data-stu-id="2ccd6-258">5</span></span>|  
|<span data-ttu-id="2ccd6-259">01-15-20</span><span class="sxs-lookup"><span data-stu-id="2ccd6-259">01-15-20</span></span>|<span data-ttu-id="2ccd6-260">[KSV-konto]</span><span class="sxs-lookup"><span data-stu-id="2ccd6-260">[COGS Account]</span></span>|<span data-ttu-id="2ccd6-261">7290</span><span class="sxs-lookup"><span data-stu-id="2ccd6-261">7290</span></span>||<span data-ttu-id="2ccd6-262">80.00</span><span class="sxs-lookup"><span data-stu-id="2ccd6-262">80.00</span></span>|<span data-ttu-id="2ccd6-263">6</span><span class="sxs-lookup"><span data-stu-id="2ccd6-263">6</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="2ccd6-264">Bokföringsdatumet för redovisningstransaktionerna är samma som för de relaterade värdetransaktionerna.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-264">The posting date of the general ledger entries is the same as for the related value entries.</span></span>  
>   
>  <span data-ttu-id="2ccd6-265">Fältet **Kostnad bokförd i redov** i tabellen **Värdetransaktion**.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-265">The **Cost Posted to G/L** field in the **Value Entry** table is filled.</span></span>  

 <span data-ttu-id="2ccd6-266">Relationen mellan värdetransaktioner och bokföringstransaktioner lagras i tabellen **Artikeltrans.relation**.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-266">The relation between value entries and general ledger entries is stored in the **G/L - Item Ledger Relation** table.</span></span>  

 <span data-ttu-id="2ccd6-267">**Relationstransaktioner i redovisning – tabellen Artikeltransaktionsrelation**</span><span class="sxs-lookup"><span data-stu-id="2ccd6-267">**Relation Entries in the G/L – Item Ledger Relation table**</span></span>  

|<span data-ttu-id="2ccd6-268">Löpnr redovisning</span><span class="sxs-lookup"><span data-stu-id="2ccd6-268">G/L Entry No.</span></span>|<span data-ttu-id="2ccd6-269">Värdelöpnr</span><span class="sxs-lookup"><span data-stu-id="2ccd6-269">Value Entry No.</span></span>|<span data-ttu-id="2ccd6-270">Bokf. redov.journalnr</span><span class="sxs-lookup"><span data-stu-id="2ccd6-270">G/L Register No.</span></span>|  
|--------------------|---------------------|-----------------------|  
|<span data-ttu-id="2ccd6-271">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-271">1</span></span>|<span data-ttu-id="2ccd6-272">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-272">1</span></span>|<span data-ttu-id="2ccd6-273">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-273">1</span></span>|  
|<span data-ttu-id="2ccd6-274">2</span><span class="sxs-lookup"><span data-stu-id="2ccd6-274">2</span></span>|<span data-ttu-id="2ccd6-275">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-275">1</span></span>|<span data-ttu-id="2ccd6-276">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-276">1</span></span>|  
|<span data-ttu-id="2ccd6-277">3</span><span class="sxs-lookup"><span data-stu-id="2ccd6-277">3</span></span>|<span data-ttu-id="2ccd6-278">2</span><span class="sxs-lookup"><span data-stu-id="2ccd6-278">2</span></span>|<span data-ttu-id="2ccd6-279">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-279">1</span></span>|  
|<span data-ttu-id="2ccd6-280">4</span><span class="sxs-lookup"><span data-stu-id="2ccd6-280">4</span></span>|<span data-ttu-id="2ccd6-281">2</span><span class="sxs-lookup"><span data-stu-id="2ccd6-281">2</span></span>|<span data-ttu-id="2ccd6-282">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-282">1</span></span>|  
|<span data-ttu-id="2ccd6-283">5</span><span class="sxs-lookup"><span data-stu-id="2ccd6-283">5</span></span>|<span data-ttu-id="2ccd6-284">3</span><span class="sxs-lookup"><span data-stu-id="2ccd6-284">3</span></span>|<span data-ttu-id="2ccd6-285">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-285">1</span></span>|  
|<span data-ttu-id="2ccd6-286">6</span><span class="sxs-lookup"><span data-stu-id="2ccd6-286">6</span></span>|<span data-ttu-id="2ccd6-287">3</span><span class="sxs-lookup"><span data-stu-id="2ccd6-287">3</span></span>|<span data-ttu-id="2ccd6-288">1</span><span class="sxs-lookup"><span data-stu-id="2ccd6-288">1</span></span>|  

## <a name="assembly-and-production-posting"></a><span data-ttu-id="2ccd6-289">Montering- och produktionsbokföring</span><span class="sxs-lookup"><span data-stu-id="2ccd6-289">Assembly and Production Posting</span></span>  
<span data-ttu-id="2ccd6-290">Kapacitets - och resurstransaktioner representerar den tid som bokförs som förbrukad i produktionen eller monteringen.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-290">Capacity and resource ledger entries represent the time that is posted as consumed in production or assembly.</span></span> <span data-ttu-id="2ccd6-291">Dessa bearbetningskostnader bokförs som värdetransaktioner i redovisningen tillsammans med relevanta materialkostnader i en liknande struktur som den som beskrivs för artikeltransaktioner i det här avsnittet.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-291">These process costs are posted as value entries to the general ledger along with the involved material costs in a similar structure as described for item ledger entries in this topic.</span></span>  

<span data-ttu-id="2ccd6-292">Mer information finns i [Designdetaljer: Bokföring av monteringsorder](design-details-assembly-order-posting.md)</span><span class="sxs-lookup"><span data-stu-id="2ccd6-292">For more information, see [Design Details: Assembly Order Posting](design-details-assembly-order-posting.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="2ccd6-293">Se även</span><span class="sxs-lookup"><span data-stu-id="2ccd6-293">See Also</span></span>  
 <span data-ttu-id="2ccd6-294">[Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md) </span><span class="sxs-lookup"><span data-stu-id="2ccd6-294">[Design Details: Inventory Costing](design-details-inventory-costing.md) </span></span>  
 <span data-ttu-id="2ccd6-295">[Designdetaljer: Konton i redovisningen](design-details-accounts-in-the-general-ledger.md) </span><span class="sxs-lookup"><span data-stu-id="2ccd6-295">[Design Details: Accounts in the General Ledger](design-details-accounts-in-the-general-ledger.md) </span></span>  
 <span data-ttu-id="2ccd6-296">[Designdetaljer: Kostnadskomponenter](design-details-cost-components.md) [Hantera lagerkostnader](finance-manage-inventory-costs.md)</span><span class="sxs-lookup"><span data-stu-id="2ccd6-296">[Design Details: Cost Components](design-details-cost-components.md) [Managing Inventory Costs](finance-manage-inventory-costs.md)</span></span>  
 [<span data-ttu-id="2ccd6-297">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="2ccd6-297">Finance</span></span>](finance.md)  
 <span data-ttu-id="2ccd6-298">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2ccd6-298">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
