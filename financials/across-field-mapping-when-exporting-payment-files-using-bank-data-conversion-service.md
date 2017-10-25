---
title: "Fältmappning för export av bankbetalningsfiler | Microsoft Docs"
description: "När du exporterar betalningsfiler med hjälp av funktionen för bankdatakonvertering kommer de data du exporterar att bli exponerade för bankdatakonverteringstjänsten."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: f81d6dac79817d758ff0ae49322a18f1e5cdc9d8
ms.contentlocale: sv-se
ms.lasthandoff: 09/27/2017

---
# <a name="field-mapping-when-exporting-payment-files-using-bank-data-conversion-service"></a><span data-ttu-id="62bca-103">Fältmappning vid export av betalningsfiler via bankdatakonverteringstjänst</span><span class="sxs-lookup"><span data-stu-id="62bca-103">Field Mapping When Exporting Payment Files Using Bank Data Conversion Service</span></span>
<span data-ttu-id="62bca-104">När du exporterar betalningsfiler med hjälp av funktionen för bankdatakonvertering kommer de data du exporterar att bli exponerade för bankdatakonverteringstjänsten.</span><span class="sxs-lookup"><span data-stu-id="62bca-104">When you export payment files using the Bank Data Conversion Service feature, the data that you export is exposed to the provider of the bank data conversion service.</span></span> <span data-ttu-id="62bca-105">Serviceleverantören är ansvarig för sekretessen för dessa data.</span><span class="sxs-lookup"><span data-stu-id="62bca-105">The service provider is responsible for the privacy of this data.</span></span> <span data-ttu-id="62bca-106">Mer information om hur funktionen bankdatakonverteringstjänst fungerar finns i [Om ramverket för datautbyte](across-about-the-data-exchange-framework.md).</span><span class="sxs-lookup"><span data-stu-id="62bca-106">For more information about how the Bank Data Conversion Service feature works, see [About the Data Exchange Framework](across-about-the-data-exchange-framework.md).</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="62bca-107">När du exporterar betalningsfiler med hjälp av funktionen för bankdatakonvertering kommer vissa av dina affärsdata att bli exponerade för tjänstleverantören.</span><span class="sxs-lookup"><span data-stu-id="62bca-107">When you export payment files by using the Bank Data Conversion Service feature, some of your business data will be exposed to the provider of the service.</span></span> <span data-ttu-id="62bca-108">Serviceleverantören, AMC Consult A/S, är ansvarig för sekretessen för dessa data.</span><span class="sxs-lookup"><span data-stu-id="62bca-108">The service provider, AMC Consult A/S, is responsible for the privacy of this data.</span></span> <span data-ttu-id="62bca-109">Mer information finns i [Sekretesspolicy för AMC](http://go.microsoft.com/fwlink/?LinkId=510158).</span><span class="sxs-lookup"><span data-stu-id="62bca-109">For more information, see [AMC Privacy Policy](http://go.microsoft.com/fwlink/?LinkId=510158).</span></span>  

<span data-ttu-id="62bca-110">Följande tabell visar de fält i [!INCLUDE[d365fin](includes/d365fin_md.md)] från vilka data kan exporteras till tjänstleverantören.</span><span class="sxs-lookup"><span data-stu-id="62bca-110">The following table lists the fields in [!INCLUDE[d365fin](includes/d365fin_md.md)] from which data can be exported to the service provider.</span></span>  

|<span data-ttu-id="62bca-111">Mappat fält</span><span class="sxs-lookup"><span data-stu-id="62bca-111">Mapped Field</span></span>|<span data-ttu-id="62bca-112">Fält i tabell</span><span class="sxs-lookup"><span data-stu-id="62bca-112">Field in Table</span></span>|<span data-ttu-id="62bca-113">Bord</span><span class="sxs-lookup"><span data-stu-id="62bca-113">Table</span></span>|<span data-ttu-id="62bca-114">Beskrivning]--></span><span class="sxs-lookup"><span data-stu-id="62bca-114">Description]--></span></span>|  
|------------------|--------------------|-----------|---------------------------------------|  
|<span data-ttu-id="62bca-115">Fordringsägarenr.</span><span class="sxs-lookup"><span data-stu-id="62bca-115">Creditor No.</span></span>|<span data-ttu-id="62bca-116">Fordringsägarenr.</span><span class="sxs-lookup"><span data-stu-id="62bca-116">Creditor No.</span></span>|<span data-ttu-id="62bca-117">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-117">Bank Account</span></span>|<span data-ttu-id="62bca-118">Den identifierare som tilldelas ditt företag av din bank för att kräva in betalningar</span><span class="sxs-lookup"><span data-stu-id="62bca-118">The identifier assigned to your company by your bank to collect payments</span></span>|  
|<span data-ttu-id="62bca-119">Avsändarens bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="62bca-119">Sender Bank Account No.</span></span>|<span data-ttu-id="62bca-120">Bankkontonr/IBAN</span><span class="sxs-lookup"><span data-stu-id="62bca-120">Bank Account No./IBAN</span></span>|<span data-ttu-id="62bca-121">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-121">Bank Account</span></span>|<span data-ttu-id="62bca-122">Företagets bankkontonummer (IBAN eller annat) som registreras på bankkontokortet</span><span class="sxs-lookup"><span data-stu-id="62bca-122">Your company's bank account number (IBAN or other) that is specified on the bank account card</span></span>|  
|<span data-ttu-id="62bca-123">Avsändarens bankclearingstandard</span><span class="sxs-lookup"><span data-stu-id="62bca-123">Sender Bank Clearing Standard</span></span>|<span data-ttu-id="62bca-124">Bankclearingstandard</span><span class="sxs-lookup"><span data-stu-id="62bca-124">Bank Clearing Standard</span></span>|<span data-ttu-id="62bca-125">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-125">Bank Account</span></span>|<span data-ttu-id="62bca-126">Den nationella bankens register som användes för avsändarens bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-126">The national bank names register used for the sender bank account</span></span>|  
|<span data-ttu-id="62bca-127">Avsändarbankens clearingnr</span><span class="sxs-lookup"><span data-stu-id="62bca-127">Sender Bank Clearing Code</span></span>|<span data-ttu-id="62bca-128">Bankclearingnummer</span><span class="sxs-lookup"><span data-stu-id="62bca-128">Bank Clearing Code</span></span>|<span data-ttu-id="62bca-129">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-129">Bank Account</span></span>|<span data-ttu-id="62bca-130">Identifieraren för avsändarens bank i förhållande till bankens namnregister som används</span><span class="sxs-lookup"><span data-stu-id="62bca-130">The identifier of the sender's bank in relation to the bank names register used</span></span>|  
|<span data-ttu-id="62bca-131">Avsändarbankens BIC-nr</span><span class="sxs-lookup"><span data-stu-id="62bca-131">Sender Bank BIC</span></span>|<span data-ttu-id="62bca-132">SWIFT kod</span><span class="sxs-lookup"><span data-stu-id="62bca-132">SWIFT Code</span></span>|<span data-ttu-id="62bca-133">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-133">Bank Account</span></span>|<span data-ttu-id="62bca-134">SWIFT-identifieraren för avsändarens bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-134">The SWIFT identifier of the sender bank account</span></span>|  
|<span data-ttu-id="62bca-135">Avsändarbankens kontovaluta</span><span class="sxs-lookup"><span data-stu-id="62bca-135">Sender Bank Account Currency</span></span>|<span data-ttu-id="62bca-136">Valutakod</span><span class="sxs-lookup"><span data-stu-id="62bca-136">Currency Code</span></span>|<span data-ttu-id="62bca-137">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-137">Bank Account</span></span>|<span data-ttu-id="62bca-138">Valutakod för avsändarens bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-138">The sender bank account Currency Code</span></span>|  
|<span data-ttu-id="62bca-139">Verifikationsnr</span><span class="sxs-lookup"><span data-stu-id="62bca-139">Document No.</span></span>|<span data-ttu-id="62bca-140">Verifikationsnr</span><span class="sxs-lookup"><span data-stu-id="62bca-140">Document No.</span></span>|<span data-ttu-id="62bca-141">Redovisningsjournalrad</span><span class="sxs-lookup"><span data-stu-id="62bca-141">General Journal Line</span></span>|<span data-ttu-id="62bca-142">Betalningsradens dokumentnummer</span><span class="sxs-lookup"><span data-stu-id="62bca-142">The document number of the payment line</span></span>|  
|<span data-ttu-id="62bca-143">Kopplas till externt dok.nr</span><span class="sxs-lookup"><span data-stu-id="62bca-143">Applies-to Ext. Doc. No.</span></span>|<span data-ttu-id="62bca-144">Kopplas till externt dok.nr</span><span class="sxs-lookup"><span data-stu-id="62bca-144">Applies-to Ext. Doc. No.</span></span>|<span data-ttu-id="62bca-145">Redovisningsjournalrad</span><span class="sxs-lookup"><span data-stu-id="62bca-145">General Journal Line</span></span>|<span data-ttu-id="62bca-146">Det externa dokumentnummer på fakturan eller kreditnotan ska betalningsraden ska kopplas till.</span><span class="sxs-lookup"><span data-stu-id="62bca-146">The external document number of the invoice or credit memo that the payment line is applied to</span></span>|  
|<span data-ttu-id="62bca-147">Mottagarens ID</span><span class="sxs-lookup"><span data-stu-id="62bca-147">Recipient ID</span></span>|<span data-ttu-id="62bca-148">Kontonr</span><span class="sxs-lookup"><span data-stu-id="62bca-148">Account No.</span></span>|<span data-ttu-id="62bca-149">Redovisningsjournalrad</span><span class="sxs-lookup"><span data-stu-id="62bca-149">General Journal Line</span></span>|<span data-ttu-id="62bca-150">Numret för den kund eller leverantör som specificeras på betalningsraden</span><span class="sxs-lookup"><span data-stu-id="62bca-150">The customer or vendor number that is specified on the payment line</span></span>|  
|<span data-ttu-id="62bca-151">Betalningsform</span><span class="sxs-lookup"><span data-stu-id="62bca-151">Payment Type</span></span>|<span data-ttu-id="62bca-152">Bet.typ för bankdatakonvertering</span><span class="sxs-lookup"><span data-stu-id="62bca-152">Bank Data Conversion Pmt. Type</span></span>|<span data-ttu-id="62bca-153">Betalningssätt</span><span class="sxs-lookup"><span data-stu-id="62bca-153">Payment Method</span></span>|<span data-ttu-id="62bca-154">Typen av banköverföring, till exempel inrikes eller internationell</span><span class="sxs-lookup"><span data-stu-id="62bca-154">The type of bank transfer, such as domestic or international</span></span>|  
|<span data-ttu-id="62bca-155">Betalningsreferens</span><span class="sxs-lookup"><span data-stu-id="62bca-155">Payment Reference</span></span>|<span data-ttu-id="62bca-156">Betalningsreferens</span><span class="sxs-lookup"><span data-stu-id="62bca-156">Payment Reference</span></span>|<span data-ttu-id="62bca-157">Redovisningsjournalrad</span><span class="sxs-lookup"><span data-stu-id="62bca-157">General Journal Line</span></span>|<span data-ttu-id="62bca-158">Betalningsradens betalningsreferens</span><span class="sxs-lookup"><span data-stu-id="62bca-158">The payment reference of the payment line</span></span>|  
|<span data-ttu-id="62bca-159">Mottagarens adress</span><span class="sxs-lookup"><span data-stu-id="62bca-159">Recipient Address</span></span>|<span data-ttu-id="62bca-160">Adress</span><span class="sxs-lookup"><span data-stu-id="62bca-160">Address</span></span>|<span data-ttu-id="62bca-161">Kund/Leverantör</span><span class="sxs-lookup"><span data-stu-id="62bca-161">Customer/Vendor</span></span>|<span data-ttu-id="62bca-162">Mottagaradressen som anges på kund- eller leverantörskortet</span><span class="sxs-lookup"><span data-stu-id="62bca-162">The recipient address that is specified on the customer or vendor card</span></span>|  
|<span data-ttu-id="62bca-163">Mottagarens ort</span><span class="sxs-lookup"><span data-stu-id="62bca-163">Recipient City</span></span>|<span data-ttu-id="62bca-164">Stad</span><span class="sxs-lookup"><span data-stu-id="62bca-164">City</span></span>|<span data-ttu-id="62bca-165">Kund/Leverantör</span><span class="sxs-lookup"><span data-stu-id="62bca-165">Customer/Vendor</span></span>|<span data-ttu-id="62bca-166">Mottagarens stad som anges på kund- eller leverantörskortet</span><span class="sxs-lookup"><span data-stu-id="62bca-166">The recipient city that is specified on the customer or vendor card</span></span>|  
|<span data-ttu-id="62bca-167">Mottagarens namn</span><span class="sxs-lookup"><span data-stu-id="62bca-167">Recipient Name</span></span>|<span data-ttu-id="62bca-168">Namn</span><span class="sxs-lookup"><span data-stu-id="62bca-168">Name</span></span>|<span data-ttu-id="62bca-169">Kund/Leverantör</span><span class="sxs-lookup"><span data-stu-id="62bca-169">Customer/Vendor</span></span>|<span data-ttu-id="62bca-170">Mottagarens namn som anges på kund- eller leverantörskortet</span><span class="sxs-lookup"><span data-stu-id="62bca-170">The recipient name that is specified on the customer or vendor card</span></span>|  
|<span data-ttu-id="62bca-171">Mottagarens lands-/regionkod</span><span class="sxs-lookup"><span data-stu-id="62bca-171">Recipient Country/Region Code</span></span>|<span data-ttu-id="62bca-172">Lands-/regionkod</span><span class="sxs-lookup"><span data-stu-id="62bca-172">Country/Region Code</span></span>|<span data-ttu-id="62bca-173">Kund/Leverantör</span><span class="sxs-lookup"><span data-stu-id="62bca-173">Customer/Vendor</span></span>|<span data-ttu-id="62bca-174">Mottagarens kod för land/region som anges på kundens eller leverantörens bankkontokort</span><span class="sxs-lookup"><span data-stu-id="62bca-174">The recipient country/region code that is specified on the customer or vendor card</span></span>|  
|<span data-ttu-id="62bca-175">Mottagarens postnr</span><span class="sxs-lookup"><span data-stu-id="62bca-175">Recipient Post Code</span></span>|<span data-ttu-id="62bca-176">Postnr</span><span class="sxs-lookup"><span data-stu-id="62bca-176">Post Code</span></span>|<span data-ttu-id="62bca-177">Kund/Leverantör</span><span class="sxs-lookup"><span data-stu-id="62bca-177">Customer/Vendor</span></span>|<span data-ttu-id="62bca-178">Mottagarens postnummer för land/region som anges på kundens eller leverantörens bankkontokort</span><span class="sxs-lookup"><span data-stu-id="62bca-178">The recipient post code that is specified on the customer or vendor card</span></span>|  
|<span data-ttu-id="62bca-179">Mottagarbankens kontonr</span><span class="sxs-lookup"><span data-stu-id="62bca-179">Recipient Bank Acc. No.</span></span>|<span data-ttu-id="62bca-180">Bankkontonr/IBAN</span><span class="sxs-lookup"><span data-stu-id="62bca-180">Bank Account No./IBAN</span></span>|<span data-ttu-id="62bca-181">Kund bankkonto/Leverantör bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-181">Customer Bank Account/Vendor Bank Account</span></span>|<span data-ttu-id="62bca-182">Mottagarens bankkontonummer (IBAN eller annat nummer) som anges på kundens eller leverantörens bankkontokort</span><span class="sxs-lookup"><span data-stu-id="62bca-182">The recipient bank account number (IBAN or other) that is specified on the customer or vendor bank account card</span></span>|  
|<span data-ttu-id="62bca-183">Mottagarbankens clearingnr</span><span class="sxs-lookup"><span data-stu-id="62bca-183">Recipient Bank Clearing Code</span></span>|<span data-ttu-id="62bca-184">Bankclearingstandard</span><span class="sxs-lookup"><span data-stu-id="62bca-184">Bank Clearing Standard</span></span>|<span data-ttu-id="62bca-185">Kund bankkonto/Leverantör bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-185">Customer Bank Account/Vendor Bank Account</span></span>|<span data-ttu-id="62bca-186">Den nationella bankens register som användes för mottagarens bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-186">The national bank names register used for the recipient bank account</span></span>|  
|<span data-ttu-id="62bca-187">Mottagarbankens clearingst.</span><span class="sxs-lookup"><span data-stu-id="62bca-187">Recipient Bank Clearing Std.</span></span>|<span data-ttu-id="62bca-188">Bankclearingnummer</span><span class="sxs-lookup"><span data-stu-id="62bca-188">Bank Clearing Code</span></span>|<span data-ttu-id="62bca-189">Kund bankkonto/Leverantör bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-189">Customer Bank Account/Vendor Bank Account</span></span>|<span data-ttu-id="62bca-190">Identifieraren för mottagarens bankkonto i förhållande till bankens namnregister som används</span><span class="sxs-lookup"><span data-stu-id="62bca-190">The identifier of the recipient bank account in relation to the bank names register that is used</span></span>|  
|<span data-ttu-id="62bca-191">Mottagarens e-postadress</span><span class="sxs-lookup"><span data-stu-id="62bca-191">Recipient Email Address</span></span>|<span data-ttu-id="62bca-192">E-post</span><span class="sxs-lookup"><span data-stu-id="62bca-192">E-Mail</span></span>|<span data-ttu-id="62bca-193">Kund/Leverantör</span><span class="sxs-lookup"><span data-stu-id="62bca-193">Customer/Vendor</span></span>|<span data-ttu-id="62bca-194">E-postadressen till mottagaren</span><span class="sxs-lookup"><span data-stu-id="62bca-194">The email address of the recipient</span></span>|  
|<span data-ttu-id="62bca-195">Meddelande till mottagare 1</span><span class="sxs-lookup"><span data-stu-id="62bca-195">Message To Recipient 1</span></span>|<span data-ttu-id="62bca-196">Meddelande till mottagare</span><span class="sxs-lookup"><span data-stu-id="62bca-196">Message to Recipient</span></span>|<span data-ttu-id="62bca-197">Redovisningsjournalrad</span><span class="sxs-lookup"><span data-stu-id="62bca-197">General Journal Line</span></span>|<span data-ttu-id="62bca-198">Meddelandet till mottagaren som anges på betalningsraden</span><span class="sxs-lookup"><span data-stu-id="62bca-198">The message to recipient that is specified on the payment line</span></span>|  
|<span data-ttu-id="62bca-199">Belopp</span><span class="sxs-lookup"><span data-stu-id="62bca-199">Amount</span></span>|<span data-ttu-id="62bca-200">Belopp</span><span class="sxs-lookup"><span data-stu-id="62bca-200">Amount</span></span>|<span data-ttu-id="62bca-201">Redovisningsjournalrad</span><span class="sxs-lookup"><span data-stu-id="62bca-201">General Journal Line</span></span>|<span data-ttu-id="62bca-202">Beloppet på betalningsraden</span><span class="sxs-lookup"><span data-stu-id="62bca-202">The amount on the payment line</span></span>|  
|<span data-ttu-id="62bca-203">Valutakod</span><span class="sxs-lookup"><span data-stu-id="62bca-203">Currency Code</span></span>|<span data-ttu-id="62bca-204">Valutakod</span><span class="sxs-lookup"><span data-stu-id="62bca-204">Currency Code</span></span>|<span data-ttu-id="62bca-205">Redovisningsjournalrad</span><span class="sxs-lookup"><span data-stu-id="62bca-205">General Journal Line</span></span>|<span data-ttu-id="62bca-206">Valutakoden på betalningsraden</span><span class="sxs-lookup"><span data-stu-id="62bca-206">The currency code on the payment line</span></span>|  
|<span data-ttu-id="62bca-207">Överföringsdatum</span><span class="sxs-lookup"><span data-stu-id="62bca-207">Transfer Date</span></span>|<span data-ttu-id="62bca-208">Bokföringsdatum</span><span class="sxs-lookup"><span data-stu-id="62bca-208">Posting Date</span></span>|<span data-ttu-id="62bca-209">Redovisningsjournalrad</span><span class="sxs-lookup"><span data-stu-id="62bca-209">General Journal Line</span></span>|<span data-ttu-id="62bca-210">Bokföringsdatumet för betalningsraden</span><span class="sxs-lookup"><span data-stu-id="62bca-210">The posting date of the payment line</span></span>|  
|<span data-ttu-id="62bca-211">Fakturabelopp</span><span class="sxs-lookup"><span data-stu-id="62bca-211">Invoice Amount</span></span>|<span data-ttu-id="62bca-212">Ursprungligt belopp</span><span class="sxs-lookup"><span data-stu-id="62bca-212">Original Amount</span></span>|<span data-ttu-id="62bca-213">Kund/Lev.reskontratransaktion</span><span class="sxs-lookup"><span data-stu-id="62bca-213">Customer/Vendor Ledger Entry</span></span>|<span data-ttu-id="62bca-214">Beloppet på den transaktion som betalningen kopplas till.</span><span class="sxs-lookup"><span data-stu-id="62bca-214">The amount on the entry that the payment is applied to</span></span>|  
|<span data-ttu-id="62bca-215">Fakturadatum</span><span class="sxs-lookup"><span data-stu-id="62bca-215">Invoice Date</span></span>|<span data-ttu-id="62bca-216">Dokumentdatum</span><span class="sxs-lookup"><span data-stu-id="62bca-216">Document Date</span></span>|<span data-ttu-id="62bca-217">Kund/Lev.reskontratransaktion</span><span class="sxs-lookup"><span data-stu-id="62bca-217">Customer/Vendor Ledger Entry</span></span>|<span data-ttu-id="62bca-218">Fakturadatumet på den transaktion som betalningen kopplas till</span><span class="sxs-lookup"><span data-stu-id="62bca-218">The invoice date on the entry that the payment is applied to</span></span>|  
|<span data-ttu-id="62bca-219">Mottagarbankens adress</span><span class="sxs-lookup"><span data-stu-id="62bca-219">Recipient Bank Address</span></span>|<span data-ttu-id="62bca-220">Adress</span><span class="sxs-lookup"><span data-stu-id="62bca-220">Address</span></span>|<span data-ttu-id="62bca-221">Kund bankkonto/Leverantör bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-221">Customer Bank Account/Vendor Bank Account</span></span>|<span data-ttu-id="62bca-222">Mottagarens adress för bankkontot som anges på kundens eller leverantörens bankkontokort</span><span class="sxs-lookup"><span data-stu-id="62bca-222">The recipient bank account address that is specified on the customer or vendor bank account card</span></span>|  
|<span data-ttu-id="62bca-223">Mottagarens adress för bankkontot som anges på kundens eller leverantörens bankkontokort</span><span class="sxs-lookup"><span data-stu-id="62bca-223">The recipient bank account address that is specified on the customer or vendor bank account card</span></span>|<span data-ttu-id="62bca-224">Stad</span><span class="sxs-lookup"><span data-stu-id="62bca-224">City</span></span>|<span data-ttu-id="62bca-225">Kund bankkonto/Leverantör bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-225">Customer Bank Account/Vendor Bank Account</span></span>|<span data-ttu-id="62bca-226">Mottagarens stad för bankkontot som anges på kundens eller leverantörens bankkontokort</span><span class="sxs-lookup"><span data-stu-id="62bca-226">The recipient bank account city that is specified on the customer or vendor bank account card</span></span>|  
|<span data-ttu-id="62bca-227">Mottagarbankens namn</span><span class="sxs-lookup"><span data-stu-id="62bca-227">Recipient Bank Name</span></span>|<span data-ttu-id="62bca-228">Namn</span><span class="sxs-lookup"><span data-stu-id="62bca-228">Name</span></span>|<span data-ttu-id="62bca-229">Kund bankkonto/Leverantör bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-229">Customer Bank Account/Vendor Bank Account</span></span>|<span data-ttu-id="62bca-230">Mottagarens namn för bankkontot som anges på kundens eller leverantörens bankkontokort</span><span class="sxs-lookup"><span data-stu-id="62bca-230">The recipient bank account name that is specified on the customer or vendor bank account card</span></span>|  
|<span data-ttu-id="62bca-231">Mottagarbankens land/region</span><span class="sxs-lookup"><span data-stu-id="62bca-231">Recipient Bank Country/Region</span></span>|<span data-ttu-id="62bca-232">Lands-/regionkod</span><span class="sxs-lookup"><span data-stu-id="62bca-232">Country/Region Code</span></span>|<span data-ttu-id="62bca-233">Kund bankkonto/Leverantör bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-233">Customer Bank Account/Vendor Bank Account</span></span>|<span data-ttu-id="62bca-234">Mottagarens land/region för bankkontot som anges på kundens eller leverantörens bankkontokort</span><span class="sxs-lookup"><span data-stu-id="62bca-234">The recipient bank account country/region that is specified on the customer or vendor bank account card</span></span>|  
|<span data-ttu-id="62bca-235">Mottagarbankens postnr</span><span class="sxs-lookup"><span data-stu-id="62bca-235">Recipient Bank Post Code</span></span>|<span data-ttu-id="62bca-236">Postnr</span><span class="sxs-lookup"><span data-stu-id="62bca-236">Post Code</span></span>|<span data-ttu-id="62bca-237">Kund bankkonto/Leverantör bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-237">Customer Bank Account/Vendor Bank Account</span></span>|<span data-ttu-id="62bca-238">Mottagarens postnummer för bankkontot som anges på kundens eller leverantörens bankkontokort</span><span class="sxs-lookup"><span data-stu-id="62bca-238">The recipient bank account post code that is specified on the customer or vendor bank account card</span></span>|  
|<span data-ttu-id="62bca-239">Avsändarbankens adress</span><span class="sxs-lookup"><span data-stu-id="62bca-239">Sender Bank Address</span></span>|<span data-ttu-id="62bca-240">Adress</span><span class="sxs-lookup"><span data-stu-id="62bca-240">Address</span></span>|<span data-ttu-id="62bca-241">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-241">Bank Account</span></span>|<span data-ttu-id="62bca-242">Den adress för avsändarens bankkonto som anges på bankkontokortet</span><span class="sxs-lookup"><span data-stu-id="62bca-242">The sender bank account address that is specified on the bank account card</span></span>|  
|<span data-ttu-id="62bca-243">Avsändarbankens ort</span><span class="sxs-lookup"><span data-stu-id="62bca-243">Sender Bank City</span></span>|<span data-ttu-id="62bca-244">Stad</span><span class="sxs-lookup"><span data-stu-id="62bca-244">City</span></span>|<span data-ttu-id="62bca-245">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-245">Bank Account</span></span>|<span data-ttu-id="62bca-246">Den stad för avsändarens bankkonto som anges på bankkontokortet</span><span class="sxs-lookup"><span data-stu-id="62bca-246">The sender bank account city that is specified on the bank account card</span></span>|  
|<span data-ttu-id="62bca-247">Avsändarbankens namn</span><span class="sxs-lookup"><span data-stu-id="62bca-247">Sender Bank Name</span></span>|<span data-ttu-id="62bca-248">Namn</span><span class="sxs-lookup"><span data-stu-id="62bca-248">Name</span></span>|<span data-ttu-id="62bca-249">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-249">Bank Account</span></span>|<span data-ttu-id="62bca-250">Det namn för avsändarens bankkonto som anges på bankkontokortet</span><span class="sxs-lookup"><span data-stu-id="62bca-250">The sender bank account name that is specified on the bank account card</span></span>|  
|<span data-ttu-id="62bca-251">Avsändarbankens land/region</span><span class="sxs-lookup"><span data-stu-id="62bca-251">Sender Bank Country/Region</span></span>|<span data-ttu-id="62bca-252">Lands-/regionkod</span><span class="sxs-lookup"><span data-stu-id="62bca-252">Country/Region Code</span></span>|<span data-ttu-id="62bca-253">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-253">Bank Account</span></span>|<span data-ttu-id="62bca-254">Landet/regionen för avsändarens bankkonto som anges på bankkontokortet</span><span class="sxs-lookup"><span data-stu-id="62bca-254">The sender bank account country/region that is specified on the bank account card</span></span>|  
|<span data-ttu-id="62bca-255">Avsändarbankens postnr</span><span class="sxs-lookup"><span data-stu-id="62bca-255">Sender Bank Post Code</span></span>|<span data-ttu-id="62bca-256">Postnr</span><span class="sxs-lookup"><span data-stu-id="62bca-256">Post Code</span></span>|<span data-ttu-id="62bca-257">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-257">Bank Account</span></span>|<span data-ttu-id="62bca-258">Det postnummer för avsändarens bankkonto som anges på bankkontokortet</span><span class="sxs-lookup"><span data-stu-id="62bca-258">The sender bank account post code that is specified on the bank account card</span></span>|  
|<span data-ttu-id="62bca-259">Redovisningsjournalmall</span><span class="sxs-lookup"><span data-stu-id="62bca-259">General Journal Template</span></span>|<span data-ttu-id="62bca-260">Mallnamn för journal</span><span class="sxs-lookup"><span data-stu-id="62bca-260">Journal Template Name</span></span>|<span data-ttu-id="62bca-261">Redovisningsjournalrad</span><span class="sxs-lookup"><span data-stu-id="62bca-261">General Journal Line</span></span>|<span data-ttu-id="62bca-262">Redovisningsjournalens mall som används för betalningsraden</span><span class="sxs-lookup"><span data-stu-id="62bca-262">The general journal template that is used for the payment line</span></span>|  
|<span data-ttu-id="62bca-263">Redovisningsjournalnamn</span><span class="sxs-lookup"><span data-stu-id="62bca-263">General Journal Batch Name</span></span>|<span data-ttu-id="62bca-264">Journalnamn</span><span class="sxs-lookup"><span data-stu-id="62bca-264">Journal Batch Name</span></span>|<span data-ttu-id="62bca-265">Redovisningsjournalrad</span><span class="sxs-lookup"><span data-stu-id="62bca-265">General Journal Line</span></span>|<span data-ttu-id="62bca-266">Redovisningsjournalens batchnamn som används för betalningsraden</span><span class="sxs-lookup"><span data-stu-id="62bca-266">The general journal batch name that is used for the payment line</span></span>|  
|<span data-ttu-id="62bca-267">Avsändarbankens namn – datakonv.</span><span class="sxs-lookup"><span data-stu-id="62bca-267">Sender Bank Name - Data Conv.</span></span>|<span data-ttu-id="62bca-268">Banknamn – datakonvertering</span><span class="sxs-lookup"><span data-stu-id="62bca-268">Bank Name – Data Conv.</span></span>|<span data-ttu-id="62bca-269">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="62bca-269">Bank Account</span></span>|<span data-ttu-id="62bca-270">Avsändarens bankkontonamn som begärs av bankdatakonverteringstjänsten och anges på bankkontokortet</span><span class="sxs-lookup"><span data-stu-id="62bca-270">The sender bank account name that is requested by the bank data conversion service and specified on the bank account card</span></span>|  

## <a name="see-also"></a><span data-ttu-id="62bca-271">Se även</span><span class="sxs-lookup"><span data-stu-id="62bca-271">See Also</span></span>  
[<span data-ttu-id="62bca-272">Konfigurera datautbyte</span><span class="sxs-lookup"><span data-stu-id="62bca-272">Setting Up Data Exchange</span></span>](across-set-up-data-exchange.md)  
<span data-ttu-id="62bca-273">[Utbyta data elektroniskt](across-data-exchange.md)
[Så här konfigurerar du bankdatakonverteringstjänsten](bank-how-setup-bank-data-conversion-service.md) </span><span class="sxs-lookup"><span data-stu-id="62bca-273">[Exchanging Data Electronically](across-data-exchange.md)
[How to: Set Up the Bank Data Conversion Service](bank-how-setup-bank-data-conversion-service.md) </span></span>  
[<span data-ttu-id="62bca-274">Gör betalningar med tjänsten för bankdatakonvertering eller SEPA Kreditöverföring</span><span class="sxs-lookup"><span data-stu-id="62bca-274">Make Payments with Bank Data Conversion Service or SEPA Credit Transfer</span></span>](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)   
