---
title: Designdetaljer - Konton i redovisningen | Microsoft Docs
description: "Om du vill stämma av lager- och kapacitetstransaktioner med redovisningen, bokförs de relaterade värdetransaktionerna på olika redovisningskonton."
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
ms.openlocfilehash: a9d313a4fee3dedf74cc2f0c635516397e26d8ef
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-accounts-in-the-general-ledger"></a><span data-ttu-id="47ef7-103">Designdetaljer: Konton i redovisningen</span><span class="sxs-lookup"><span data-stu-id="47ef7-103">Design Details: Accounts in the General Ledger</span></span>
<span data-ttu-id="47ef7-104">Om du vill stämma av lager- och kapacitetstransaktioner med redovisningen, bokförs de relaterade värdetransaktionerna på olika redovisningskonton.</span><span class="sxs-lookup"><span data-stu-id="47ef7-104">To reconcile inventory and capacity ledger entries with the general ledger, the related value entries are posted to different accounts in the general ledger.</span></span> <span data-ttu-id="47ef7-105">Mer information finns i [detaljer: avstämning med redovisningen](design-details-reconciliation-with-the-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="47ef7-105">For more information, see [Design Details: Reconciliation with the General Ledger](design-details-reconciliation-with-the-general-ledger.md).</span></span>  

## <a name="from-the-inventory-ledger"></a><span data-ttu-id="47ef7-106">Från inventeringstransaktioner</span><span class="sxs-lookup"><span data-stu-id="47ef7-106">From the Inventory Ledger</span></span>  
<span data-ttu-id="47ef7-107">Följande tabell visar relationen mellan olika typer av lagervärdetransaktioner och konton och motkonton i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="47ef7-107">The following table shows the relationship between different types of inventory value entries and the accounts and balancing accounts in the general ledger.</span></span>  

|<span data-ttu-id="47ef7-108">**Artikeltransaktionstyp**</span><span class="sxs-lookup"><span data-stu-id="47ef7-108">**Item Ledger Entry Type**</span></span>|<span data-ttu-id="47ef7-109">**Värdetrans.typ**</span><span class="sxs-lookup"><span data-stu-id="47ef7-109">**Value Entry Ttype**</span></span>|<span data-ttu-id="47ef7-110">**Varianstyp**</span><span class="sxs-lookup"><span data-stu-id="47ef7-110">**Variance Type**</span></span>|<span data-ttu-id="47ef7-111">**Förväntad kostnad**</span><span class="sxs-lookup"><span data-stu-id="47ef7-111">**Expected Cost**</span></span>|<span data-ttu-id="47ef7-112">**Konto**</span><span class="sxs-lookup"><span data-stu-id="47ef7-112">**Account**</span></span>|<span data-ttu-id="47ef7-113">**Balanskonto**</span><span class="sxs-lookup"><span data-stu-id="47ef7-113">**Balancing Account**</span></span>|  
|--------------------------------|--------------------------|-----------------------|-----------------------|-----------------|---------------------------|  
|<span data-ttu-id="47ef7-114">Inköp</span><span class="sxs-lookup"><span data-stu-id="47ef7-114">Purchase</span></span>|<span data-ttu-id="47ef7-115">Direkt kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-115">Direct Cost</span></span>||<span data-ttu-id="47ef7-116">Ja</span><span class="sxs-lookup"><span data-stu-id="47ef7-116">Yes</span></span>|<span data-ttu-id="47ef7-117">Lager (interim)</span><span class="sxs-lookup"><span data-stu-id="47ef7-117">Inventory  (Interim)</span></span>|<span data-ttu-id="47ef7-118">Lagerbokf. (interim)</span><span class="sxs-lookup"><span data-stu-id="47ef7-118">Invt. Accrual Acc. (Interim)</span></span>|  
|<span data-ttu-id="47ef7-119">Inköp</span><span class="sxs-lookup"><span data-stu-id="47ef7-119">Purchase</span></span>|<span data-ttu-id="47ef7-120">Direkt kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-120">Direct Cost</span></span>||<span data-ttu-id="47ef7-121">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-121">No</span></span>|<span data-ttu-id="47ef7-122">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-122">Inventory</span></span>|<span data-ttu-id="47ef7-123">Direkt kostnad kopplad</span><span class="sxs-lookup"><span data-stu-id="47ef7-123">Direct Cost Applied</span></span>|  
|<span data-ttu-id="47ef7-124">Inköp</span><span class="sxs-lookup"><span data-stu-id="47ef7-124">Purchase</span></span>|<span data-ttu-id="47ef7-125">Indirekt kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-125">Indirect Cost</span></span>||<span data-ttu-id="47ef7-126">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-126">No</span></span>|<span data-ttu-id="47ef7-127">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-127">Inventory</span></span>|<span data-ttu-id="47ef7-128">Omkostnader kopplade</span><span class="sxs-lookup"><span data-stu-id="47ef7-128">Overhead Applied</span></span>|  
|<span data-ttu-id="47ef7-129">Inköp</span><span class="sxs-lookup"><span data-stu-id="47ef7-129">Purchase</span></span>|<span data-ttu-id="47ef7-130">Varians</span><span class="sxs-lookup"><span data-stu-id="47ef7-130">Variance</span></span>|<span data-ttu-id="47ef7-131">Inköp</span><span class="sxs-lookup"><span data-stu-id="47ef7-131">Purchase</span></span>|<span data-ttu-id="47ef7-132">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-132">No</span></span>|<span data-ttu-id="47ef7-133">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-133">Inventory</span></span>|<span data-ttu-id="47ef7-134">Inköpsvarians</span><span class="sxs-lookup"><span data-stu-id="47ef7-134">Purchase Variance</span></span>|  
|<span data-ttu-id="47ef7-135">Inköp</span><span class="sxs-lookup"><span data-stu-id="47ef7-135">Purchase</span></span>|<span data-ttu-id="47ef7-136">Omvärdering</span><span class="sxs-lookup"><span data-stu-id="47ef7-136">Revaluation</span></span>||<span data-ttu-id="47ef7-137">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-137">No</span></span>|<span data-ttu-id="47ef7-138">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-138">Inventory</span></span>|<span data-ttu-id="47ef7-139">Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="47ef7-139">Inventory Adjmt.</span></span>|  
|<span data-ttu-id="47ef7-140">Inköp</span><span class="sxs-lookup"><span data-stu-id="47ef7-140">Purchase</span></span>|<span data-ttu-id="47ef7-141">Avrundning</span><span class="sxs-lookup"><span data-stu-id="47ef7-141">Rounding</span></span>||<span data-ttu-id="47ef7-142">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-142">No</span></span>|<span data-ttu-id="47ef7-143">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-143">Inventory</span></span>|<span data-ttu-id="47ef7-144">Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="47ef7-144">Inventory Adjmt.</span></span>|  
|<span data-ttu-id="47ef7-145">Försäljning</span><span class="sxs-lookup"><span data-stu-id="47ef7-145">Sale</span></span>|<span data-ttu-id="47ef7-146">Direkt kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-146">Direct Cost</span></span>||<span data-ttu-id="47ef7-147">Ja</span><span class="sxs-lookup"><span data-stu-id="47ef7-147">Yes</span></span>|<span data-ttu-id="47ef7-148">Lager (interim)</span><span class="sxs-lookup"><span data-stu-id="47ef7-148">Inventory  (Interim)</span></span>|<span data-ttu-id="47ef7-149">KSV (interim)</span><span class="sxs-lookup"><span data-stu-id="47ef7-149">COGS (Interim)</span></span>|  
|<span data-ttu-id="47ef7-150">Försäljning</span><span class="sxs-lookup"><span data-stu-id="47ef7-150">Sale</span></span>|<span data-ttu-id="47ef7-151">Direkt kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-151">Direct Cost</span></span>||<span data-ttu-id="47ef7-152">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-152">No</span></span>|<span data-ttu-id="47ef7-153">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-153">Inventory</span></span>|<span data-ttu-id="47ef7-154">KSV</span><span class="sxs-lookup"><span data-stu-id="47ef7-154">COGS</span></span>|  
|<span data-ttu-id="47ef7-155">Försäljning</span><span class="sxs-lookup"><span data-stu-id="47ef7-155">Sale</span></span>|<span data-ttu-id="47ef7-156">Omvärdering</span><span class="sxs-lookup"><span data-stu-id="47ef7-156">Revaluation</span></span>||<span data-ttu-id="47ef7-157">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-157">No</span></span>|<span data-ttu-id="47ef7-158">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-158">Inventory</span></span>|<span data-ttu-id="47ef7-159">Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="47ef7-159">Inventory Adjmt.</span></span>|  
|<span data-ttu-id="47ef7-160">Försäljning</span><span class="sxs-lookup"><span data-stu-id="47ef7-160">Sale</span></span>|<span data-ttu-id="47ef7-161">Avrundning</span><span class="sxs-lookup"><span data-stu-id="47ef7-161">Rounding</span></span>||<span data-ttu-id="47ef7-162">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-162">No</span></span>|<span data-ttu-id="47ef7-163">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-163">Inventory</span></span>|<span data-ttu-id="47ef7-164">Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="47ef7-164">Inventory Adjmt.</span></span>|  
|<span data-ttu-id="47ef7-165">Positiv justering,Negativ justering,Överföring</span><span class="sxs-lookup"><span data-stu-id="47ef7-165">Positive Adjmt.,Negative Adjmt., Transfer</span></span>|<span data-ttu-id="47ef7-166">Direkt kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-166">Direct Cost</span></span>||<span data-ttu-id="47ef7-167">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-167">No</span></span>|<span data-ttu-id="47ef7-168">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-168">Inventory</span></span>|<span data-ttu-id="47ef7-169">Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="47ef7-169">Inventory Adjmt.</span></span>|  
|<span data-ttu-id="47ef7-170">Positiv justering,Negativ justering,Överföring</span><span class="sxs-lookup"><span data-stu-id="47ef7-170">Positive Adjmt.,Negative Adjmt., Transfer</span></span>|<span data-ttu-id="47ef7-171">Omvärdering</span><span class="sxs-lookup"><span data-stu-id="47ef7-171">Revaluation</span></span>||<span data-ttu-id="47ef7-172">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-172">No</span></span>|<span data-ttu-id="47ef7-173">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-173">Inventory</span></span>|<span data-ttu-id="47ef7-174">Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="47ef7-174">Inventory Adjmt.</span></span>|  
|<span data-ttu-id="47ef7-175">Positiv justering,Negativ justering,Överföring</span><span class="sxs-lookup"><span data-stu-id="47ef7-175">Positive Adjmt.,Negative Adjmt., Transfer</span></span>|<span data-ttu-id="47ef7-176">Avrundning</span><span class="sxs-lookup"><span data-stu-id="47ef7-176">Rounding</span></span>||<span data-ttu-id="47ef7-177">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-177">No</span></span>|<span data-ttu-id="47ef7-178">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-178">Inventory</span></span>|<span data-ttu-id="47ef7-179">Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="47ef7-179">Inventory Adjmt.</span></span>|  
|<span data-ttu-id="47ef7-180">(Produktion) Förbrukning</span><span class="sxs-lookup"><span data-stu-id="47ef7-180">(Production) Consumption</span></span>|<span data-ttu-id="47ef7-181">Direkt kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-181">Direct Cost</span></span>||<span data-ttu-id="47ef7-182">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-182">No</span></span>|<span data-ttu-id="47ef7-183">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-183">Inventory</span></span>|<span data-ttu-id="47ef7-184">PIA</span><span class="sxs-lookup"><span data-stu-id="47ef7-184">WIP</span></span>|  
|<span data-ttu-id="47ef7-185">(Produktion) Förbrukning</span><span class="sxs-lookup"><span data-stu-id="47ef7-185">(Production) Consumption</span></span>|<span data-ttu-id="47ef7-186">Omvärdering</span><span class="sxs-lookup"><span data-stu-id="47ef7-186">Revaluation</span></span>||<span data-ttu-id="47ef7-187">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-187">No</span></span>|<span data-ttu-id="47ef7-188">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-188">Inventory</span></span>|<span data-ttu-id="47ef7-189">Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="47ef7-189">Inventory Adjmt.</span></span>|  
|<span data-ttu-id="47ef7-190">(Produktion) Förbrukning</span><span class="sxs-lookup"><span data-stu-id="47ef7-190">(Production) Consumption</span></span>|<span data-ttu-id="47ef7-191">Avrundning</span><span class="sxs-lookup"><span data-stu-id="47ef7-191">Rounding</span></span>||<span data-ttu-id="47ef7-192">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-192">No</span></span>|<span data-ttu-id="47ef7-193">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-193">Inventory</span></span>|<span data-ttu-id="47ef7-194">Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="47ef7-194">Inventory Adjmt.</span></span>|  
|<span data-ttu-id="47ef7-195">Monteringsförbrukning</span><span class="sxs-lookup"><span data-stu-id="47ef7-195">Assembly Consumption</span></span>|<span data-ttu-id="47ef7-196">Direkt kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-196">Direct Cost</span></span>||<span data-ttu-id="47ef7-197">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-197">No</span></span>|<span data-ttu-id="47ef7-198">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-198">Inventory</span></span>|<span data-ttu-id="47ef7-199">Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="47ef7-199">Inventory Adjmt.</span></span>|  
|<span data-ttu-id="47ef7-200">Monteringsförbrukning</span><span class="sxs-lookup"><span data-stu-id="47ef7-200">Assembly Consumption</span></span>|<span data-ttu-id="47ef7-201">Direkt kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-201">Direct Cost</span></span>||<span data-ttu-id="47ef7-202">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-202">No</span></span>|<span data-ttu-id="47ef7-203">Direkt kostnad kopplad</span><span class="sxs-lookup"><span data-stu-id="47ef7-203">Direct Cost Applied</span></span>|<span data-ttu-id="47ef7-204">Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="47ef7-204">Inventory Adjmt.</span></span>|  
|<span data-ttu-id="47ef7-205">Monteringsförbrukning</span><span class="sxs-lookup"><span data-stu-id="47ef7-205">Assembly Consumption</span></span>|<span data-ttu-id="47ef7-206">Indirekt kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-206">Indirect Cost</span></span>||<span data-ttu-id="47ef7-207">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-207">No</span></span>|<span data-ttu-id="47ef7-208">Omkostnader kopplade</span><span class="sxs-lookup"><span data-stu-id="47ef7-208">Overhead Applied</span></span>|<span data-ttu-id="47ef7-209">Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="47ef7-209">Inventory Adjmt.</span></span>|  
|<span data-ttu-id="47ef7-210">(Produktions)utflöde</span><span class="sxs-lookup"><span data-stu-id="47ef7-210">(Production) Output</span></span>|<span data-ttu-id="47ef7-211">Direkt kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-211">Direct Cost</span></span>||<span data-ttu-id="47ef7-212">Ja</span><span class="sxs-lookup"><span data-stu-id="47ef7-212">Yes</span></span>|<span data-ttu-id="47ef7-213">Lager (interim)</span><span class="sxs-lookup"><span data-stu-id="47ef7-213">Inventory  (Interim)</span></span>|<span data-ttu-id="47ef7-214">PIA</span><span class="sxs-lookup"><span data-stu-id="47ef7-214">WIP</span></span>|  
|<span data-ttu-id="47ef7-215">(Produktions)utflöde</span><span class="sxs-lookup"><span data-stu-id="47ef7-215">(Production) Output</span></span>|<span data-ttu-id="47ef7-216">Direkt kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-216">Direct Cost</span></span>||<span data-ttu-id="47ef7-217">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-217">No</span></span>|<span data-ttu-id="47ef7-218">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-218">Inventory</span></span>|<span data-ttu-id="47ef7-219">PIA</span><span class="sxs-lookup"><span data-stu-id="47ef7-219">WIP</span></span>|  
|<span data-ttu-id="47ef7-220">(Produktions)utflöde</span><span class="sxs-lookup"><span data-stu-id="47ef7-220">(Production) Output</span></span>|<span data-ttu-id="47ef7-221">Indirekt kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-221">Indirect Cost</span></span>||<span data-ttu-id="47ef7-222">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-222">No</span></span>|<span data-ttu-id="47ef7-223">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-223">Inventory</span></span>|<span data-ttu-id="47ef7-224">Omkostnader kopplade</span><span class="sxs-lookup"><span data-stu-id="47ef7-224">Overhead Applied</span></span>|  
|<span data-ttu-id="47ef7-225">(Produktions)utflöde</span><span class="sxs-lookup"><span data-stu-id="47ef7-225">(Production) Output</span></span>|<span data-ttu-id="47ef7-226">Varians</span><span class="sxs-lookup"><span data-stu-id="47ef7-226">Variance</span></span>|<span data-ttu-id="47ef7-227">Material</span><span class="sxs-lookup"><span data-stu-id="47ef7-227">Material</span></span>|<span data-ttu-id="47ef7-228">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-228">No</span></span>|<span data-ttu-id="47ef7-229">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-229">Inventory</span></span>|<span data-ttu-id="47ef7-230">Materialvarians</span><span class="sxs-lookup"><span data-stu-id="47ef7-230">Material Variance</span></span>|  
|<span data-ttu-id="47ef7-231">(Produktions)utflöde</span><span class="sxs-lookup"><span data-stu-id="47ef7-231">(Production) Output</span></span>|<span data-ttu-id="47ef7-232">Varians</span><span class="sxs-lookup"><span data-stu-id="47ef7-232">Variance</span></span>|<span data-ttu-id="47ef7-233">Kapacitet</span><span class="sxs-lookup"><span data-stu-id="47ef7-233">Capacity</span></span>|<span data-ttu-id="47ef7-234">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-234">No</span></span>|<span data-ttu-id="47ef7-235">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-235">Inventory</span></span>|<span data-ttu-id="47ef7-236">Kapacitetsvarians</span><span class="sxs-lookup"><span data-stu-id="47ef7-236">Capacity Variance</span></span>|  
|<span data-ttu-id="47ef7-237">(Produktions)utflöde</span><span class="sxs-lookup"><span data-stu-id="47ef7-237">(Production) Output</span></span>|<span data-ttu-id="47ef7-238">Varians</span><span class="sxs-lookup"><span data-stu-id="47ef7-238">Variance</span></span>|<span data-ttu-id="47ef7-239">Legotillverkning</span><span class="sxs-lookup"><span data-stu-id="47ef7-239">Subcontracted</span></span>|<span data-ttu-id="47ef7-240">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-240">No</span></span>|<span data-ttu-id="47ef7-241">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-241">Inventory</span></span>|<span data-ttu-id="47ef7-242">Legotillverkning varians</span><span class="sxs-lookup"><span data-stu-id="47ef7-242">Subcontracted Variance</span></span>|  
|<span data-ttu-id="47ef7-243">(Produktions)utflöde</span><span class="sxs-lookup"><span data-stu-id="47ef7-243">(Production) Output</span></span>|<span data-ttu-id="47ef7-244">Varians</span><span class="sxs-lookup"><span data-stu-id="47ef7-244">Variance</span></span>|<span data-ttu-id="47ef7-245">Kapacitetsomkostnader</span><span class="sxs-lookup"><span data-stu-id="47ef7-245">Capacity Overhead</span></span>|<span data-ttu-id="47ef7-246">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-246">No</span></span>|<span data-ttu-id="47ef7-247">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-247">Inventory</span></span>|<span data-ttu-id="47ef7-248">Kapacitetsomkostnader varians</span><span class="sxs-lookup"><span data-stu-id="47ef7-248">Cap. Overhead Variance</span></span>|  
|<span data-ttu-id="47ef7-249">(Produktions)utflöde</span><span class="sxs-lookup"><span data-stu-id="47ef7-249">(Production) Output</span></span>|<span data-ttu-id="47ef7-250">Varians</span><span class="sxs-lookup"><span data-stu-id="47ef7-250">Variance</span></span>|<span data-ttu-id="47ef7-251">Produktionsomkostnader</span><span class="sxs-lookup"><span data-stu-id="47ef7-251">Manufacturing Overhead</span></span>|<span data-ttu-id="47ef7-252">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-252">No</span></span>|<span data-ttu-id="47ef7-253">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-253">Inventory</span></span>|<span data-ttu-id="47ef7-254">Prod.- och omkostnadsvarians</span><span class="sxs-lookup"><span data-stu-id="47ef7-254">Mfg. Overhead Variance</span></span>|  
|<span data-ttu-id="47ef7-255">(Produktions)utflöde</span><span class="sxs-lookup"><span data-stu-id="47ef7-255">(Production) Output</span></span>|<span data-ttu-id="47ef7-256">Omvärdering</span><span class="sxs-lookup"><span data-stu-id="47ef7-256">Revaluation</span></span>||<span data-ttu-id="47ef7-257">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-257">No</span></span>|<span data-ttu-id="47ef7-258">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-258">Inventory</span></span>|<span data-ttu-id="47ef7-259">Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="47ef7-259">Inventory Adjmt.</span></span>|  
|<span data-ttu-id="47ef7-260">(Produktions)utflöde</span><span class="sxs-lookup"><span data-stu-id="47ef7-260">(Production) Output</span></span>|<span data-ttu-id="47ef7-261">Avrundning</span><span class="sxs-lookup"><span data-stu-id="47ef7-261">Rounding</span></span>||<span data-ttu-id="47ef7-262">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-262">No</span></span>|<span data-ttu-id="47ef7-263">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-263">Inventory</span></span>|<span data-ttu-id="47ef7-264">Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="47ef7-264">Inventory Adjmt.</span></span>|  
|<span data-ttu-id="47ef7-265">Monteringsutflöde</span><span class="sxs-lookup"><span data-stu-id="47ef7-265">Assembly Output</span></span>|<span data-ttu-id="47ef7-266">Direkt kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-266">Direct Cost</span></span>||<span data-ttu-id="47ef7-267">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-267">No</span></span>|<span data-ttu-id="47ef7-268">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-268">Inventory</span></span>|<span data-ttu-id="47ef7-269">Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="47ef7-269">Inventory Adjmt.</span></span>|  
|<span data-ttu-id="47ef7-270">Monteringsutflöde</span><span class="sxs-lookup"><span data-stu-id="47ef7-270">Assembly Output</span></span>|<span data-ttu-id="47ef7-271">Omvärdering</span><span class="sxs-lookup"><span data-stu-id="47ef7-271">Revaluation</span></span>||<span data-ttu-id="47ef7-272">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-272">No</span></span>|<span data-ttu-id="47ef7-273">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-273">Inventory</span></span>|<span data-ttu-id="47ef7-274">Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="47ef7-274">Inventory Adjmt.</span></span>|  
|<span data-ttu-id="47ef7-275">Monteringsutflöde</span><span class="sxs-lookup"><span data-stu-id="47ef7-275">Assembly Output</span></span>|<span data-ttu-id="47ef7-276">Indirekt kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-276">Indirect Cost</span></span>||<span data-ttu-id="47ef7-277">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-277">No</span></span>|<span data-ttu-id="47ef7-278">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-278">Inventory</span></span>|<span data-ttu-id="47ef7-279">Omkostnader kopplade</span><span class="sxs-lookup"><span data-stu-id="47ef7-279">Overhead Applied</span></span>|  
|<span data-ttu-id="47ef7-280">Monteringsutflöde</span><span class="sxs-lookup"><span data-stu-id="47ef7-280">Assembly Output</span></span>|<span data-ttu-id="47ef7-281">Varians</span><span class="sxs-lookup"><span data-stu-id="47ef7-281">Variance</span></span>|<span data-ttu-id="47ef7-282">Material</span><span class="sxs-lookup"><span data-stu-id="47ef7-282">Material</span></span>|<span data-ttu-id="47ef7-283">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-283">No</span></span>|<span data-ttu-id="47ef7-284">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-284">Inventory</span></span>|<span data-ttu-id="47ef7-285">Materialvarians</span><span class="sxs-lookup"><span data-stu-id="47ef7-285">Material Variance</span></span>|  
|<span data-ttu-id="47ef7-286">Monteringsutflöde</span><span class="sxs-lookup"><span data-stu-id="47ef7-286">Assembly Output</span></span>|<span data-ttu-id="47ef7-287">Varians</span><span class="sxs-lookup"><span data-stu-id="47ef7-287">Variance</span></span>|<span data-ttu-id="47ef7-288">Kapacitet</span><span class="sxs-lookup"><span data-stu-id="47ef7-288">Capacity</span></span>|<span data-ttu-id="47ef7-289">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-289">No</span></span>|<span data-ttu-id="47ef7-290">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-290">Inventory</span></span>|<span data-ttu-id="47ef7-291">Kapacitetsvarians</span><span class="sxs-lookup"><span data-stu-id="47ef7-291">Capacity Variance</span></span>|  
|<span data-ttu-id="47ef7-292">Monteringsutflöde</span><span class="sxs-lookup"><span data-stu-id="47ef7-292">Assembly Output</span></span>|<span data-ttu-id="47ef7-293">Varians</span><span class="sxs-lookup"><span data-stu-id="47ef7-293">Variance</span></span>|<span data-ttu-id="47ef7-294">Kapacitetsomkostnader</span><span class="sxs-lookup"><span data-stu-id="47ef7-294">Capacity Overhead</span></span>|<span data-ttu-id="47ef7-295">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-295">No</span></span>|<span data-ttu-id="47ef7-296">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-296">Inventory</span></span>|<span data-ttu-id="47ef7-297">Kapacitetsomkostnader varians</span><span class="sxs-lookup"><span data-stu-id="47ef7-297">Cap. Overhead Variance</span></span>|  
|<span data-ttu-id="47ef7-298">Monteringsutflöde</span><span class="sxs-lookup"><span data-stu-id="47ef7-298">Assembly Output</span></span>|<span data-ttu-id="47ef7-299">Varians</span><span class="sxs-lookup"><span data-stu-id="47ef7-299">Variance</span></span>|<span data-ttu-id="47ef7-300">Produktionsomkostnader</span><span class="sxs-lookup"><span data-stu-id="47ef7-300">Manufacturing Overhead</span></span>|<span data-ttu-id="47ef7-301">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-301">No</span></span>|<span data-ttu-id="47ef7-302">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-302">Inventory</span></span>|<span data-ttu-id="47ef7-303">Prod.- och omkostnadsvarians</span><span class="sxs-lookup"><span data-stu-id="47ef7-303">Mfg. Overhead Variance</span></span>|  
|<span data-ttu-id="47ef7-304">Monteringsutflöde</span><span class="sxs-lookup"><span data-stu-id="47ef7-304">Assembly Output</span></span>|<span data-ttu-id="47ef7-305">Avrundning</span><span class="sxs-lookup"><span data-stu-id="47ef7-305">Rounding</span></span>||<span data-ttu-id="47ef7-306">Nr</span><span class="sxs-lookup"><span data-stu-id="47ef7-306">No</span></span>|<span data-ttu-id="47ef7-307">Lagersaldo</span><span class="sxs-lookup"><span data-stu-id="47ef7-307">Inventory</span></span>|<span data-ttu-id="47ef7-308">Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="47ef7-308">Inventory Adjmt.</span></span>|  

## <a name="from-the-capacity-ledger"></a><span data-ttu-id="47ef7-309">Från kapacitetstransaktioner</span><span class="sxs-lookup"><span data-stu-id="47ef7-309">From the Capacity Ledger</span></span>  
 <span data-ttu-id="47ef7-310">Följande tabell visar relationen mellan olika typer av kapacitetvärdetransaktioner och konton och motkonton i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="47ef7-310">The following table shows the relationship between different types of capacity value entries and the accounts and balancing accounts in the general ledger.</span></span> <span data-ttu-id="47ef7-311">Kapacitetstransaktioner representerar arbetstid som förbrukats vid monterings- eller produktionsarbete.</span><span class="sxs-lookup"><span data-stu-id="47ef7-311">Capacity ledger entries represent labor time consumed in assembly or production work.</span></span>  

|<span data-ttu-id="47ef7-312">**Arbetstyp**</span><span class="sxs-lookup"><span data-stu-id="47ef7-312">**Work Type**</span></span>|<span data-ttu-id="47ef7-313">**Kapacitetstrans. typ**</span><span class="sxs-lookup"><span data-stu-id="47ef7-313">**Capacity Ledger Entry Type**</span></span>|<span data-ttu-id="47ef7-314">**Värdetrans.typ**</span><span class="sxs-lookup"><span data-stu-id="47ef7-314">**Value Entry Type**</span></span>|<span data-ttu-id="47ef7-315">**Konto**</span><span class="sxs-lookup"><span data-stu-id="47ef7-315">**Account**</span></span>|<span data-ttu-id="47ef7-316">**Balanskonto**</span><span class="sxs-lookup"><span data-stu-id="47ef7-316">**Balancing Account**</span></span>|  
|-------------------|------------------------------------|--------------------------|-----------------|---------------------------|  
|<span data-ttu-id="47ef7-317">Montering</span><span class="sxs-lookup"><span data-stu-id="47ef7-317">Assembly</span></span>|<span data-ttu-id="47ef7-318">Resurs</span><span class="sxs-lookup"><span data-stu-id="47ef7-318">Resource</span></span>|<span data-ttu-id="47ef7-319">Direkt kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-319">Direct Cost</span></span>|<span data-ttu-id="47ef7-320">Direkt kostnad kopplad</span><span class="sxs-lookup"><span data-stu-id="47ef7-320">Direct Cost Applied</span></span>|<span data-ttu-id="47ef7-321">Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="47ef7-321">Inventory Adjmt.</span></span>|  
|<span data-ttu-id="47ef7-322">Montering</span><span class="sxs-lookup"><span data-stu-id="47ef7-322">Assembly</span></span>|<span data-ttu-id="47ef7-323">Resurs</span><span class="sxs-lookup"><span data-stu-id="47ef7-323">Resource</span></span>|<span data-ttu-id="47ef7-324">Indirekt kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-324">Indirect Cost</span></span>|<span data-ttu-id="47ef7-325">Omkostnader kopplade</span><span class="sxs-lookup"><span data-stu-id="47ef7-325">Overhead Applied</span></span>|<span data-ttu-id="47ef7-326">Lagerjustering</span><span class="sxs-lookup"><span data-stu-id="47ef7-326">Inventory Adjmt.</span></span>|  
|<span data-ttu-id="47ef7-327">Produktion</span><span class="sxs-lookup"><span data-stu-id="47ef7-327">Production</span></span>|<span data-ttu-id="47ef7-328">Maskingrupp/Produktionsgrupp</span><span class="sxs-lookup"><span data-stu-id="47ef7-328">Machine Center/Work Center</span></span>|<span data-ttu-id="47ef7-329">Inköpskostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-329">Direct Cost</span></span>|<span data-ttu-id="47ef7-330">PIA-konto</span><span class="sxs-lookup"><span data-stu-id="47ef7-330">WIP Account</span></span>|<span data-ttu-id="47ef7-331">Direkt kostnad kopplad</span><span class="sxs-lookup"><span data-stu-id="47ef7-331">Direct Cost Applied</span></span>|  
|<span data-ttu-id="47ef7-332">Produktion</span><span class="sxs-lookup"><span data-stu-id="47ef7-332">Production</span></span>|<span data-ttu-id="47ef7-333">Maskingrupp/Produktionsgrupp</span><span class="sxs-lookup"><span data-stu-id="47ef7-333">Machine Center/Work Center</span></span>|<span data-ttu-id="47ef7-334">Indirekt kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-334">Indirect Cost</span></span>|<span data-ttu-id="47ef7-335">PIA-konto</span><span class="sxs-lookup"><span data-stu-id="47ef7-335">WIP Account</span></span>|<span data-ttu-id="47ef7-336">Omkostnader kopplade</span><span class="sxs-lookup"><span data-stu-id="47ef7-336">Overhead Applied</span></span>|  

## <a name="assembly-costs-are-always-actual"></a><span data-ttu-id="47ef7-337">Monteringkostnader är alltid faktiska</span><span class="sxs-lookup"><span data-stu-id="47ef7-337">Assembly Costs are Always Actual</span></span>  
 <span data-ttu-id="47ef7-338">Som visas i tabellen ovan visas inte bokföringar av montering i interimskonton.</span><span class="sxs-lookup"><span data-stu-id="47ef7-338">As shown in the table above, assembly postings are not represented in interim accounts.</span></span> <span data-ttu-id="47ef7-339">Det beror på att konceptet med produkter i arbete (PIA) inte är tillämpligt i monteringsutflödesbokföring, till skillnad från i produktionsutflödesbokföring.</span><span class="sxs-lookup"><span data-stu-id="47ef7-339">This is because the concept of work in process (WIP) does not apply in assembly output posting, unlike in production output posting.</span></span> <span data-ttu-id="47ef7-340">Monteringkostnader bokförs bara som faktiska kostnader, aldrig som förväntade kostnader.</span><span class="sxs-lookup"><span data-stu-id="47ef7-340">Assembly costs are only posted as actual cost, never as expected cost.</span></span>  

 <span data-ttu-id="47ef7-341">Mer information finns i [Designdetaljer: Bokföring av monteringsorder](design-details-assembly-order-posting.md)</span><span class="sxs-lookup"><span data-stu-id="47ef7-341">For more information, see [Design Details: Assembly Order Posting](design-details-assembly-order-posting.md).</span></span>  

## <a name="calculating-the-amount-to-post-to-the-general-ledger"></a><span data-ttu-id="47ef7-342">Beräknar antal att bokföra i redovisningen</span><span class="sxs-lookup"><span data-stu-id="47ef7-342">Calculating the Amount to Post to the General Ledger</span></span>  
 <span data-ttu-id="47ef7-343">Följande fält i tabellen **Värdetransaktion** används för att beräkna det förväntade kostnadsbeloppet som har bokförts i redovisningen:</span><span class="sxs-lookup"><span data-stu-id="47ef7-343">The following fields in the **Value Entry** table are used to calculate the expected cost amount that is posted to the general ledger:</span></span>  

-   <span data-ttu-id="47ef7-344">Kost.belopp (aktuellt)</span><span class="sxs-lookup"><span data-stu-id="47ef7-344">Cost Amount (Actual)</span></span>  
-   <span data-ttu-id="47ef7-345">Kostnad bokförd i redov.</span><span class="sxs-lookup"><span data-stu-id="47ef7-345">Cost Posted to G/L</span></span>  
-   <span data-ttu-id="47ef7-346">Kost.belopp (förväntat)</span><span class="sxs-lookup"><span data-stu-id="47ef7-346">Cost Amount (Expected)</span></span>  
-   <span data-ttu-id="47ef7-347">Förväntad kost. bokf. i redov.</span><span class="sxs-lookup"><span data-stu-id="47ef7-347">Expected Cost Posted to G/L</span></span>  

<span data-ttu-id="47ef7-348">Följande tabell visar hur beloppen att bokföra i redovisningen beräknas för de två olika kostnadstyperna.</span><span class="sxs-lookup"><span data-stu-id="47ef7-348">The following table shows how the amounts to post to the general ledger are calculated for the two different cost types.</span></span>  

|<span data-ttu-id="47ef7-349">Kostnadstyp</span><span class="sxs-lookup"><span data-stu-id="47ef7-349">Cost Type</span></span>|<span data-ttu-id="47ef7-350">Beräkning</span><span class="sxs-lookup"><span data-stu-id="47ef7-350">Calculation</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="47ef7-351">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-351">Actual Cost</span></span>|<span data-ttu-id="47ef7-352">Kost.belopp (aktuellt) - kostnad bokförd i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="47ef7-352">Cost Amount (Actual) – Cost Posted to G/L</span></span>|  
|<span data-ttu-id="47ef7-353">Förväntad kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-353">Expected Cost</span></span>|<span data-ttu-id="47ef7-354">Kost.belopp (förväntat) – Förväntad kost. bokf. i redov.</span><span class="sxs-lookup"><span data-stu-id="47ef7-354">Cost Amount (Expected) –  Expected Cost Posted to G/L</span></span>|  

## <a name="see-also"></a><span data-ttu-id="47ef7-355">Se även</span><span class="sxs-lookup"><span data-stu-id="47ef7-355">See Also</span></span>  
 <span data-ttu-id="47ef7-356">[Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md) </span><span class="sxs-lookup"><span data-stu-id="47ef7-356">[Design Details: Inventory Costing](design-details-inventory-costing.md) </span></span>  
 <span data-ttu-id="47ef7-357">[Designdetaljer: Lagerbokföring](design-details-inventory-posting.md) </span><span class="sxs-lookup"><span data-stu-id="47ef7-357">[Design Details: Inventory Posting](design-details-inventory-posting.md) </span></span>  
 [<span data-ttu-id="47ef7-358">Designdetaljer: Bokföring av förväntad kostnad</span><span class="sxs-lookup"><span data-stu-id="47ef7-358">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
 [<span data-ttu-id="47ef7-359">Hantera lagerkostnader</span><span class="sxs-lookup"><span data-stu-id="47ef7-359">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
 [<span data-ttu-id="47ef7-360">Ekonomi</span><span class="sxs-lookup"><span data-stu-id="47ef7-360">Finance</span></span>](finance.md)  
 <span data-ttu-id="47ef7-361">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="47ef7-361">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
