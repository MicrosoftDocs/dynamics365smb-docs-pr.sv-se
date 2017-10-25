---
title: "Designdetaljer - Bokföring av förväntad kostnad | Microsoft Docs"
description: "Förväntade kostnader representerar uppskattningen av exempelvis en inköpt artikels kostnad som du registrerar innan fakturan för artikeln erhålls."
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
ms.openlocfilehash: eae1608b8768771759ac717c59606c930472d261
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-expected-cost-posting"></a><span data-ttu-id="0dfa6-103">Designdetaljer: Bokföring av förväntad kostnad</span><span class="sxs-lookup"><span data-stu-id="0dfa6-103">Design Details: Expected Cost Posting</span></span>
<span data-ttu-id="0dfa6-104">Förväntade kostnader representerar uppskattningen av exempelvis en inköpt artikels kostnad som du registrerar innan fakturan för artikeln erhålls.</span><span class="sxs-lookup"><span data-stu-id="0dfa6-104">Expected costs represent the estimation of, for example, a purchased item’s cost that you record before you receive the invoice for the item.</span></span>  

 <span data-ttu-id="0dfa6-105">Du kan bokföra förväntade kostnader till lagret och redovisningen.</span><span class="sxs-lookup"><span data-stu-id="0dfa6-105">You can post expected cost to inventory and to the general ledger.</span></span> <span data-ttu-id="0dfa6-106">När du bokför ett antal som bara har inlevererats eller levererats men inte fakturerats, skapas en värdetransaktion med den förväntade kostnaden.</span><span class="sxs-lookup"><span data-stu-id="0dfa6-106">When you post a quantity that is only received or shipped but not invoiced, then a value entry is created with the expected cost.</span></span> <span data-ttu-id="0dfa6-107">Den förväntade kostnaden påverkar lagervärdet men bokförs inte till redovisningen om du inte har ställt in systemet att göra det.</span><span class="sxs-lookup"><span data-stu-id="0dfa6-107">This expected cost affects the inventory value, but is not posted to the general ledger unless you set up the system up to do so.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0dfa6-108">Förväntade kostnader hanteras endast för artikeltransaktioner.</span><span class="sxs-lookup"><span data-stu-id="0dfa6-108">Expected costs are only managed for item transactions.</span></span> <span data-ttu-id="0dfa6-109">Förväntade kostnader är inte för immateriella transaktionstyper, till exempel kapacitet och artikelomkostnader.</span><span class="sxs-lookup"><span data-stu-id="0dfa6-109">Expected costs are not for immaterial transaction types, such as capacity and item charges.</span></span>  

 <span data-ttu-id="0dfa6-110">Om endast antalsdelen för en lagerökning har bokförts ändras lagervärdet inte i redovisningen, om du inte har markerat kryssrutan **Förväntad kost.bokf. i redov.** i fönstret the **Lagerinställningar**.</span><span class="sxs-lookup"><span data-stu-id="0dfa6-110">If only the quantity part of an inventory increase has been posted, then the inventory value in the general ledger does not change unless you have selected the **Expected Cost Posting to G/L** check box in the **Inventory Setup** window.</span></span> <span data-ttu-id="0dfa6-111">I så fall bokförs förväntade kostnader på interimskonton vid tidpunkten för inleveransen.</span><span class="sxs-lookup"><span data-stu-id="0dfa6-111">In that case, the expected cost is posted to interim accounts at the time of receipt.</span></span> <span data-ttu-id="0dfa6-112">När inleveransen har fakturerats helt balanseras interimskontona och den faktiska kostnaden bokförs till lagerkontot.</span><span class="sxs-lookup"><span data-stu-id="0dfa6-112">After the receipt has been fully invoiced, the interim accounts are then balanced and the actual cost is posted to the inventory account.</span></span>  

 <span data-ttu-id="0dfa6-113">För att stödja avstämning och spårbarhet visar den fakturerade värdetransaktionen det förväntade kostnadsbeloppet som har bokförts för att motkontera interimskontona.</span><span class="sxs-lookup"><span data-stu-id="0dfa6-113">To support reconciliation and traceability work, the invoiced value entry shows the expected cost amount that has been posted to balance the interim accounts.</span></span>  

## <a name="example"></a><span data-ttu-id="0dfa6-114">Exempel</span><span class="sxs-lookup"><span data-stu-id="0dfa6-114">Example</span></span>  
 <span data-ttu-id="0dfa6-115">Följande exempel visar förväntade kostnaden om kryssrutan **Automatisk kostnadsbokföring** och kryssrutan **Förväntad kost.bokf. i redov.** är markerad i fönstret **Lagerinställningar**.</span><span class="sxs-lookup"><span data-stu-id="0dfa6-115">The following example shows expected cost if the **Automatic Cost Posting** check box and the **Expected Cost Posting to G/L** check box are selected in the **Inventory Setup** window.</span></span>  

 <span data-ttu-id="0dfa6-116">Du bokför en inköpsorder som mottagen.</span><span class="sxs-lookup"><span data-stu-id="0dfa6-116">You post a purchase order as received.</span></span> <span data-ttu-id="0dfa6-117">Förväntad kostnad är 95,00 BVA.</span><span class="sxs-lookup"><span data-stu-id="0dfa6-117">The expected cost is LCY 95.00.</span></span>  

 <span data-ttu-id="0dfa6-118">**Värdetransaktioner**</span><span class="sxs-lookup"><span data-stu-id="0dfa6-118">**Value Entries**</span></span>  

|<span data-ttu-id="0dfa6-119">Bokföringsdatum</span><span class="sxs-lookup"><span data-stu-id="0dfa6-119">Posting Date</span></span>|<span data-ttu-id="0dfa6-120">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="0dfa6-120">Entry Type</span></span>|<span data-ttu-id="0dfa6-121">Kost.belopp (förväntat)</span><span class="sxs-lookup"><span data-stu-id="0dfa6-121">Cost Amount (Expected)</span></span>|<span data-ttu-id="0dfa6-122">Förväntad kost. bokf. i redov.</span><span class="sxs-lookup"><span data-stu-id="0dfa6-122">Expected Cost Posted to G/L</span></span>|<span data-ttu-id="0dfa6-123">Förväntad kostnad</span><span class="sxs-lookup"><span data-stu-id="0dfa6-123">Expected Cost</span></span>|<span data-ttu-id="0dfa6-124">Artikeltrans.löpnr</span><span class="sxs-lookup"><span data-stu-id="0dfa6-124">Item Ledger Entry No.</span></span>|<span data-ttu-id="0dfa6-125">Löpnr</span><span class="sxs-lookup"><span data-stu-id="0dfa6-125">Entry No.</span></span>|  
|------------------|----------------|------------------------------|----------------------------------|-------------------|---------------------------|---------------|  
|<span data-ttu-id="0dfa6-126">01-01-20</span><span class="sxs-lookup"><span data-stu-id="0dfa6-126">01-01-20</span></span>|<span data-ttu-id="0dfa6-127">Inköpskostnad</span><span class="sxs-lookup"><span data-stu-id="0dfa6-127">Direct Cost</span></span>|<span data-ttu-id="0dfa6-128">95.00</span><span class="sxs-lookup"><span data-stu-id="0dfa6-128">95.00</span></span>|<span data-ttu-id="0dfa6-129">95.00</span><span class="sxs-lookup"><span data-stu-id="0dfa6-129">95.00</span></span>|<span data-ttu-id="0dfa6-130">Ja</span><span class="sxs-lookup"><span data-stu-id="0dfa6-130">Yes</span></span>|<span data-ttu-id="0dfa6-131">1</span><span class="sxs-lookup"><span data-stu-id="0dfa6-131">1</span></span>|<span data-ttu-id="0dfa6-132">1</span><span class="sxs-lookup"><span data-stu-id="0dfa6-132">1</span></span>|  

 <span data-ttu-id="0dfa6-133">**Relationstransaktioner i redovisning – tabellen Artikeltransaktionsrelation**</span><span class="sxs-lookup"><span data-stu-id="0dfa6-133">**Relation Entries in the G/L – Item Ledger Relation Table**</span></span>  

|<span data-ttu-id="0dfa6-134">Löpnr redovisning</span><span class="sxs-lookup"><span data-stu-id="0dfa6-134">G/L Entry No.</span></span>|<span data-ttu-id="0dfa6-135">Värdelöpnr</span><span class="sxs-lookup"><span data-stu-id="0dfa6-135">Value Entry No.</span></span>|<span data-ttu-id="0dfa6-136">Bokf. redov.journalnr</span><span class="sxs-lookup"><span data-stu-id="0dfa6-136">G/L Register No.</span></span>|  
|--------------------|---------------------|-----------------------|  
|<span data-ttu-id="0dfa6-137">1</span><span class="sxs-lookup"><span data-stu-id="0dfa6-137">1</span></span>|<span data-ttu-id="0dfa6-138">1</span><span class="sxs-lookup"><span data-stu-id="0dfa6-138">1</span></span>|<span data-ttu-id="0dfa6-139">1</span><span class="sxs-lookup"><span data-stu-id="0dfa6-139">1</span></span>|  
|<span data-ttu-id="0dfa6-140">2</span><span class="sxs-lookup"><span data-stu-id="0dfa6-140">2</span></span>|<span data-ttu-id="0dfa6-141">1</span><span class="sxs-lookup"><span data-stu-id="0dfa6-141">1</span></span>|<span data-ttu-id="0dfa6-142">1</span><span class="sxs-lookup"><span data-stu-id="0dfa6-142">1</span></span>|  

 <span data-ttu-id="0dfa6-143">**Redovisningstransaktioner**</span><span class="sxs-lookup"><span data-stu-id="0dfa6-143">**General Ledger Entries**</span></span>  

|<span data-ttu-id="0dfa6-144">Bokföringsdatum</span><span class="sxs-lookup"><span data-stu-id="0dfa6-144">Posting Date</span></span>|<span data-ttu-id="0dfa6-145">Redovisningskonto</span><span class="sxs-lookup"><span data-stu-id="0dfa6-145">G/L Account</span></span>|<span data-ttu-id="0dfa6-146">Kontonr. (En-US-demo)</span><span class="sxs-lookup"><span data-stu-id="0dfa6-146">Account No. (En-US Demo)</span></span>|<span data-ttu-id="0dfa6-147">Belopp</span><span class="sxs-lookup"><span data-stu-id="0dfa6-147">Amount</span></span>|<span data-ttu-id="0dfa6-148">Löpnr</span><span class="sxs-lookup"><span data-stu-id="0dfa6-148">Entry No.</span></span>|  
|------------------|------------------|---------------------------------|------------|---------------|  
|<span data-ttu-id="0dfa6-149">01-01-20</span><span class="sxs-lookup"><span data-stu-id="0dfa6-149">01-01-20</span></span>|<span data-ttu-id="0dfa6-150">Lagerkontoredovisning (interim)</span><span class="sxs-lookup"><span data-stu-id="0dfa6-150">Inventory Accrual Account (Interim)</span></span>|<span data-ttu-id="0dfa6-151">5530</span><span class="sxs-lookup"><span data-stu-id="0dfa6-151">5530</span></span>|<span data-ttu-id="0dfa6-152">-95.00</span><span class="sxs-lookup"><span data-stu-id="0dfa6-152">-95.00</span></span>|<span data-ttu-id="0dfa6-153">2</span><span class="sxs-lookup"><span data-stu-id="0dfa6-153">2</span></span>|  
|<span data-ttu-id="0dfa6-154">01-01-20</span><span class="sxs-lookup"><span data-stu-id="0dfa6-154">01-01-20</span></span>|<span data-ttu-id="0dfa6-155">Lager (interim)</span><span class="sxs-lookup"><span data-stu-id="0dfa6-155">Inventory Account (Interim)</span></span>|<span data-ttu-id="0dfa6-156">2131</span><span class="sxs-lookup"><span data-stu-id="0dfa6-156">2131</span></span>|<span data-ttu-id="0dfa6-157">95.00</span><span class="sxs-lookup"><span data-stu-id="0dfa6-157">95.00</span></span>|<span data-ttu-id="0dfa6-158">1</span><span class="sxs-lookup"><span data-stu-id="0dfa6-158">1</span></span>|  

 <span data-ttu-id="0dfa6-159">Du kan bokföra inköpsordern som fakturerad vid ett senare tillfälle.</span><span class="sxs-lookup"><span data-stu-id="0dfa6-159">At a later date, you post the purchase order as invoiced.</span></span> <span data-ttu-id="0dfa6-160">Fakturerad kostnad är 100,00 BVA.</span><span class="sxs-lookup"><span data-stu-id="0dfa6-160">The invoiced cost is LCY 100.00.</span></span>  

 <span data-ttu-id="0dfa6-161">**Värdetransaktioner**</span><span class="sxs-lookup"><span data-stu-id="0dfa6-161">**Value Entries**</span></span>  

|<span data-ttu-id="0dfa6-162">Bokföringsdatum</span><span class="sxs-lookup"><span data-stu-id="0dfa6-162">Posting Date</span></span>|<span data-ttu-id="0dfa6-163">Kost.belopp (aktuellt)</span><span class="sxs-lookup"><span data-stu-id="0dfa6-163">Cost Amount (Actual)</span></span>|<span data-ttu-id="0dfa6-164">Kost.belopp (förväntat)</span><span class="sxs-lookup"><span data-stu-id="0dfa6-164">Cost Amount (Expected)</span></span>|<span data-ttu-id="0dfa6-165">Kostnad bokförd i redov.</span><span class="sxs-lookup"><span data-stu-id="0dfa6-165">Cost Posted to G/L</span></span>|<span data-ttu-id="0dfa6-166">Förväntad kostnad</span><span class="sxs-lookup"><span data-stu-id="0dfa6-166">Expected Cost</span></span>|<span data-ttu-id="0dfa6-167">Artikeltrans.löpnr</span><span class="sxs-lookup"><span data-stu-id="0dfa6-167">Item Ledger Entry No.</span></span>|<span data-ttu-id="0dfa6-168">Löpnr</span><span class="sxs-lookup"><span data-stu-id="0dfa6-168">Entry No.</span></span>|  
|------------------|----------------------------|------------------------------|-------------------------|-------------------|---------------------------|---------------|  
|<span data-ttu-id="0dfa6-169">01-15-20</span><span class="sxs-lookup"><span data-stu-id="0dfa6-169">01-15-20</span></span>|<span data-ttu-id="0dfa6-170">100,00</span><span class="sxs-lookup"><span data-stu-id="0dfa6-170">100.00</span></span>|<span data-ttu-id="0dfa6-171">-95.00</span><span class="sxs-lookup"><span data-stu-id="0dfa6-171">-95.00</span></span>|<span data-ttu-id="0dfa6-172">100,00</span><span class="sxs-lookup"><span data-stu-id="0dfa6-172">100.00</span></span>|<span data-ttu-id="0dfa6-173">Nej</span><span class="sxs-lookup"><span data-stu-id="0dfa6-173">No</span></span>|<span data-ttu-id="0dfa6-174">1</span><span class="sxs-lookup"><span data-stu-id="0dfa6-174">1</span></span>|<span data-ttu-id="0dfa6-175">2</span><span class="sxs-lookup"><span data-stu-id="0dfa6-175">2</span></span>|  

 <span data-ttu-id="0dfa6-176">**Relationstransaktioner i redovisning – tabellen Artikeltransaktionsrelation**</span><span class="sxs-lookup"><span data-stu-id="0dfa6-176">**Relation Entries in the G/L – Item Ledger Relation Table**</span></span>  

|<span data-ttu-id="0dfa6-177">Löpnr redovisning</span><span class="sxs-lookup"><span data-stu-id="0dfa6-177">G/L Entry No.</span></span>|<span data-ttu-id="0dfa6-178">Värdelöpnr</span><span class="sxs-lookup"><span data-stu-id="0dfa6-178">Value Entry No.</span></span>|<span data-ttu-id="0dfa6-179">Bokf. redov.journalnr</span><span class="sxs-lookup"><span data-stu-id="0dfa6-179">G/L Register No.</span></span>|  
|--------------------|---------------------|-----------------------|  
|<span data-ttu-id="0dfa6-180">3</span><span class="sxs-lookup"><span data-stu-id="0dfa6-180">3</span></span>|<span data-ttu-id="0dfa6-181">2</span><span class="sxs-lookup"><span data-stu-id="0dfa6-181">2</span></span>|<span data-ttu-id="0dfa6-182">2</span><span class="sxs-lookup"><span data-stu-id="0dfa6-182">2</span></span>|  
|<span data-ttu-id="0dfa6-183">4</span><span class="sxs-lookup"><span data-stu-id="0dfa6-183">4</span></span>|<span data-ttu-id="0dfa6-184">2</span><span class="sxs-lookup"><span data-stu-id="0dfa6-184">2</span></span>|<span data-ttu-id="0dfa6-185">2</span><span class="sxs-lookup"><span data-stu-id="0dfa6-185">2</span></span>|  
|<span data-ttu-id="0dfa6-186">5</span><span class="sxs-lookup"><span data-stu-id="0dfa6-186">5</span></span>|<span data-ttu-id="0dfa6-187">2</span><span class="sxs-lookup"><span data-stu-id="0dfa6-187">2</span></span>|<span data-ttu-id="0dfa6-188">2</span><span class="sxs-lookup"><span data-stu-id="0dfa6-188">2</span></span>|  
|<span data-ttu-id="0dfa6-189">6</span><span class="sxs-lookup"><span data-stu-id="0dfa6-189">6</span></span>|<span data-ttu-id="0dfa6-190">2</span><span class="sxs-lookup"><span data-stu-id="0dfa6-190">2</span></span>|<span data-ttu-id="0dfa6-191">2</span><span class="sxs-lookup"><span data-stu-id="0dfa6-191">2</span></span>|  

 <span data-ttu-id="0dfa6-192">**Redovisningstransaktioner**</span><span class="sxs-lookup"><span data-stu-id="0dfa6-192">**General Ledger Entries**</span></span>  

|<span data-ttu-id="0dfa6-193">Bokföringsdatum</span><span class="sxs-lookup"><span data-stu-id="0dfa6-193">Posting Date</span></span>|<span data-ttu-id="0dfa6-194">Redovisningskonto</span><span class="sxs-lookup"><span data-stu-id="0dfa6-194">G/L Account</span></span>|<span data-ttu-id="0dfa6-195">Kontonr. (En-US-demo)</span><span class="sxs-lookup"><span data-stu-id="0dfa6-195">Account No. (En-US Demo)</span></span>|<span data-ttu-id="0dfa6-196">Belopp</span><span class="sxs-lookup"><span data-stu-id="0dfa6-196">Amount</span></span>|<span data-ttu-id="0dfa6-197">Löpnr</span><span class="sxs-lookup"><span data-stu-id="0dfa6-197">Entry No.</span></span>|  
|------------------|------------------|---------------------------------|------------|---------------|  
|<span data-ttu-id="0dfa6-198">01-15-20</span><span class="sxs-lookup"><span data-stu-id="0dfa6-198">01-15-20</span></span>|<span data-ttu-id="0dfa6-199">Lagerkontoredovisning (interim)</span><span class="sxs-lookup"><span data-stu-id="0dfa6-199">Inventory Accrual Account (Interim)</span></span>|<span data-ttu-id="0dfa6-200">5530</span><span class="sxs-lookup"><span data-stu-id="0dfa6-200">5530</span></span>|<span data-ttu-id="0dfa6-201">95.00</span><span class="sxs-lookup"><span data-stu-id="0dfa6-201">95.00</span></span>|<span data-ttu-id="0dfa6-202">4</span><span class="sxs-lookup"><span data-stu-id="0dfa6-202">4</span></span>|  
|<span data-ttu-id="0dfa6-203">01-15-20</span><span class="sxs-lookup"><span data-stu-id="0dfa6-203">01-15-20</span></span>|<span data-ttu-id="0dfa6-204">Lager (interim)</span><span class="sxs-lookup"><span data-stu-id="0dfa6-204">Inventory Account (Interim)</span></span>|<span data-ttu-id="0dfa6-205">2131</span><span class="sxs-lookup"><span data-stu-id="0dfa6-205">2131</span></span>|<span data-ttu-id="0dfa6-206">-95.00</span><span class="sxs-lookup"><span data-stu-id="0dfa6-206">-95.00</span></span>|<span data-ttu-id="0dfa6-207">3</span><span class="sxs-lookup"><span data-stu-id="0dfa6-207">3</span></span>|  
|<span data-ttu-id="0dfa6-208">01-15-20</span><span class="sxs-lookup"><span data-stu-id="0dfa6-208">01-15-20</span></span>|<span data-ttu-id="0dfa6-209">Direkt kostnad kopplad - konto</span><span class="sxs-lookup"><span data-stu-id="0dfa6-209">Direct Cost Applied Account</span></span>|<span data-ttu-id="0dfa6-210">7291</span><span class="sxs-lookup"><span data-stu-id="0dfa6-210">7291</span></span>|<span data-ttu-id="0dfa6-211">-100</span><span class="sxs-lookup"><span data-stu-id="0dfa6-211">-100</span></span>|<span data-ttu-id="0dfa6-212">6</span><span class="sxs-lookup"><span data-stu-id="0dfa6-212">6</span></span>|  
|<span data-ttu-id="0dfa6-213">01-15-20</span><span class="sxs-lookup"><span data-stu-id="0dfa6-213">01-15-20</span></span>|<span data-ttu-id="0dfa6-214">Lagerkonto</span><span class="sxs-lookup"><span data-stu-id="0dfa6-214">Inventory Account</span></span>|<span data-ttu-id="0dfa6-215">2130</span><span class="sxs-lookup"><span data-stu-id="0dfa6-215">2130</span></span>|<span data-ttu-id="0dfa6-216">100</span><span class="sxs-lookup"><span data-stu-id="0dfa6-216">100</span></span>|<span data-ttu-id="0dfa6-217">5</span><span class="sxs-lookup"><span data-stu-id="0dfa6-217">5</span></span>|  

## <a name="see-also"></a><span data-ttu-id="0dfa6-218">Se även</span><span class="sxs-lookup"><span data-stu-id="0dfa6-218">See Also</span></span>
 <span data-ttu-id="0dfa6-219">[Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md) </span><span class="sxs-lookup"><span data-stu-id="0dfa6-219">[Design Details: Inventory Costing](design-details-inventory-costing.md) </span></span>  
 <span data-ttu-id="0dfa6-220">[Designdetaljer: Kostnadsjustering](design-details-cost-adjustment.md) </span><span class="sxs-lookup"><span data-stu-id="0dfa6-220">[Design Details: Cost Adjustment](design-details-cost-adjustment.md) </span></span>  
 <span data-ttu-id="0dfa6-221">[Designdetaljer: Avstämning med redovisningen](design-details-reconciliation-with-the-general-ledger.md) </span><span class="sxs-lookup"><span data-stu-id="0dfa6-221">[Design Details: Reconciliation with the General Ledger](design-details-reconciliation-with-the-general-ledger.md) </span></span>  
 <span data-ttu-id="0dfa6-222">[Designdetaljer: Lagerbokföring](design-details-inventory-posting.md) </span><span class="sxs-lookup"><span data-stu-id="0dfa6-222">[Design Details: Inventory Posting](design-details-inventory-posting.md) </span></span>  
 [<span data-ttu-id="0dfa6-223">Designdetaljer: Varians</span><span class="sxs-lookup"><span data-stu-id="0dfa6-223">Design Details: Variance</span></span>](design-details-variance.md)  
 [<span data-ttu-id="0dfa6-224">Hantera lagerkostnader</span><span class="sxs-lookup"><span data-stu-id="0dfa6-224">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
 [<span data-ttu-id="0dfa6-225">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="0dfa6-225">Finance</span></span>](finance.md)  
 <span data-ttu-id="0dfa6-226">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0dfa6-226">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
