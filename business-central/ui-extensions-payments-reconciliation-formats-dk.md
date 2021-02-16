---
title: Använda tillägg för betalningar och avstämning (DK) | Microsoft Docs
description: Det här tillägget gör det enkelt att exportera filer som är förformaterade för att uppfylla bankkraven för elektroniska inlagor.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: c8dd465213a9882a98c1ac1623d8a093f3eecb9a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757498"
---
# <a name="the-payments-and-reconciliations-dk-extension"></a><span data-ttu-id="c5a27-103">Tillägg för betalningar och avstämning (DK).</span><span class="sxs-lookup"><span data-stu-id="c5a27-103">The Payments and Reconciliations (DK) Extension</span></span>

<span data-ttu-id="c5a27-104">Gör snabba, felfria betalninger genom att exportera filer som är specifikt formaterade för utbyte med din leverantör eller bank.</span><span class="sxs-lookup"><span data-stu-id="c5a27-104">Make fast, error-free payments by exporting files that are formatted specifically for exchanges with your vendor or bank.</span></span> <span data-ttu-id="c5a27-105">Filerna påskyndar processerna för betalning och avstämning och undviker fel som kan inträffa när du manuellt anger information på en bankwebbplats.</span><span class="sxs-lookup"><span data-stu-id="c5a27-105">These files speed up the payment and reconciliation processes, and eliminate errors that can happen when you manually enter the information on a bank website.</span></span>  

<span data-ttu-id="c5a27-106">Det här tillägget stöder filformat för flera danska banker.</span><span class="sxs-lookup"><span data-stu-id="c5a27-106">This extension supports file formats for several Danish banks.</span></span> <span data-ttu-id="c5a27-107">När du exporterar betalningsinformation till en fil, packar tillägget data i det format som krävs av din bank.</span><span class="sxs-lookup"><span data-stu-id="c5a27-107">When you export payment information to a file, the extension packages the data into the format that your bank requires.</span></span> <span data-ttu-id="c5a27-108">Formaten omfattar till exempel Bankdata-vl, V3, BEC, SDC och FIK som många olika banker använder och några som är mer specialiserade för vissa banker, till exempel Danske Bank och Nordea.</span><span class="sxs-lookup"><span data-stu-id="c5a27-108">For example, the formats include Bankdata-V3, BEC, SDC, and FIK, which many different banks use, and some that are more specialized for certain banks, for example, Danske Bank and Nordea.</span></span> <span data-ttu-id="c5a27-109">Tillägget innehåller dessutom vissa format för import och avstämning av bankutdrag.</span><span class="sxs-lookup"><span data-stu-id="c5a27-109">The extension also includes some formats for importing and reconciling bank statements.</span></span>  

> [!Note]
> <span data-ttu-id="c5a27-110">Om du vill använda tillägget måste du känna till det format som banken eller leverantör kräver.</span><span class="sxs-lookup"><span data-stu-id="c5a27-110">To use the extension, you must know the format that your bank or vendor requires.</span></span> <span data-ttu-id="c5a27-111">Vissa banker eller leverantörer tillhandahåller denna information på sina webbplatser; Du kan dock behöva kontakta deras kundservice för att hämta önskad information.</span><span class="sxs-lookup"><span data-stu-id="c5a27-111">Some banks or vendors provide this information on their websites; however, you might need to contact their customer service to get the information.</span></span>  

## <a name="supported-bank-formats"></a><span data-ttu-id="c5a27-112">Bankformat som stöds</span><span class="sxs-lookup"><span data-stu-id="c5a27-112">Supported Bank Formats</span></span>
<span data-ttu-id="c5a27-113">Det här tillägget använder följande format för betalningsfiler:</span><span class="sxs-lookup"><span data-stu-id="c5a27-113">This extension can apply the following file formats for payment files:</span></span>  

* <span data-ttu-id="c5a27-114">BANKDATA-V3</span><span class="sxs-lookup"><span data-stu-id="c5a27-114">BANKDATA-V3</span></span>  
* <span data-ttu-id="c5a27-115">BEC INDLAND</span><span class="sxs-lookup"><span data-stu-id="c5a27-115">BEC-INDLAND</span></span>  
* <span data-ttu-id="c5a27-116">BEC-CSV</span><span class="sxs-lookup"><span data-stu-id="c5a27-116">BEC-CSV</span></span>  
* <span data-ttu-id="c5a27-117">DANSKEBANK CMKV</span><span class="sxs-lookup"><span data-stu-id="c5a27-117">DANSKEBANK-CMKV</span></span>  
* <span data-ttu-id="c5a27-118">DANSKEBANK CMKXKSX</span><span class="sxs-lookup"><span data-stu-id="c5a27-118">DANSKEBANK-CMKXKSX</span></span>  
* <span data-ttu-id="c5a27-119">DANSKEBANK</span><span class="sxs-lookup"><span data-stu-id="c5a27-119">DANSKEBANK</span></span>  
* <span data-ttu-id="c5a27-120">FIK71</span><span class="sxs-lookup"><span data-stu-id="c5a27-120">FIK71</span></span>  
* <span data-ttu-id="c5a27-121">NORDEA-ERHVERV-CSV</span><span class="sxs-lookup"><span data-stu-id="c5a27-121">NORDEA-ERHVERV-CSV</span></span>  
* <span data-ttu-id="c5a27-122">NORDEA</span><span class="sxs-lookup"><span data-stu-id="c5a27-122">NORDEA</span></span>  
* <span data-ttu-id="c5a27-123">NORDEA-UNITEL-V3</span><span class="sxs-lookup"><span data-stu-id="c5a27-123">NORDEA-UNITEL-V3</span></span>  
* <span data-ttu-id="c5a27-124">SDC</span><span class="sxs-lookup"><span data-stu-id="c5a27-124">SDC</span></span>  
* <span data-ttu-id="c5a27-125">SDC CSV</span><span class="sxs-lookup"><span data-stu-id="c5a27-125">SDC-CSV</span></span>  

## <a name="to-set-up-the-extension"></a><span data-ttu-id="c5a27-126">Så här ställer du in tillägget</span><span class="sxs-lookup"><span data-stu-id="c5a27-126">To set up the extension</span></span>

<span data-ttu-id="c5a27-127">Det finns några steg för att komma igång.</span><span class="sxs-lookup"><span data-stu-id="c5a27-127">There are a few steps to get started.</span></span>  

* <span data-ttu-id="c5a27-128">Tillåt betalningsdataexport.</span><span class="sxs-lookup"><span data-stu-id="c5a27-128">Allow payment data exports.</span></span> <span data-ttu-id="c5a27-129">För att skydda dina data, är detta inte är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="c5a27-129">To help protect your data, this is not readily available.</span></span>  
* <span data-ttu-id="c5a27-130">Skapa inköpsorder och leverantörsreskontra så att du inte behöver externa verifikationsnummer på fakturor.</span><span class="sxs-lookup"><span data-stu-id="c5a27-130">Set up purchase and payables so that you do not require external document numbers on invoices.</span></span> <span data-ttu-id="c5a27-131">Om det behövs kan använda du referensnumret för att referera till en viss faktura.</span><span class="sxs-lookup"><span data-stu-id="c5a27-131">If needed, you can use the reference number to refer to a specific invoice.</span></span>  
* <span data-ttu-id="c5a27-132">Ange betalningssätt för varje leverantör.</span><span class="sxs-lookup"><span data-stu-id="c5a27-132">Specify the payment method for each vendor.</span></span> <span data-ttu-id="c5a27-133">Betalningssätt definierar hur du vill betala fakturor från leverantören.</span><span class="sxs-lookup"><span data-stu-id="c5a27-133">Payment methods define how you pay invoices from the vendor.</span></span> <span data-ttu-id="c5a27-134">Till exempel bank, kontanter, check eller konto.</span><span class="sxs-lookup"><span data-stu-id="c5a27-134">For example, Bank, Cash, Check, or Account.</span></span>  
* <span data-ttu-id="c5a27-135">Ange vilket format som ska användas för var och en av dina bankkonton.</span><span class="sxs-lookup"><span data-stu-id="c5a27-135">Specify the type of format to use for each of your bank accounts.</span></span> <span data-ttu-id="c5a27-136">Det kan t.ex. vara NORDEA, DANSKEBANK, SDC.</span><span class="sxs-lookup"><span data-stu-id="c5a27-136">For example, NORDEA, DANSKEBANK, SDC, and so on.</span></span>  

<span data-ttu-id="c5a27-137">Dessutom måste du tilldela leverantörer till en inhemsk **Gen. rörelsebokföringsmall** och en **Leverantörsbokföringsmall**.</span><span class="sxs-lookup"><span data-stu-id="c5a27-137">Additionally, you must assign vendors to a domestic **Gen. Bus. Posting Group** and a **Vendor Posting Group**.</span></span> <span data-ttu-id="c5a27-138">Inställningen av Land/Region måste för leverantören vara Danmark (DK).</span><span class="sxs-lookup"><span data-stu-id="c5a27-138">The Country/Region setting for the vendor must be Denmark (DK).</span></span> <span data-ttu-id="c5a27-139">Mer information finns i [Ställa in bokföringsmallar](finance-posting-groups.md).</span><span class="sxs-lookup"><span data-stu-id="c5a27-139">For more information, see [Setting Up Posting Groups](finance-posting-groups.md).</span></span>  

### <a name="to-allow-prod_short-to-export-payment-data"></a><span data-ttu-id="c5a27-140">För att tillåta betalningsdataexport från [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="c5a27-140">To allow [!INCLUDE[prod_short](includes/prod_short.md)] to export payment data</span></span>

1. <span data-ttu-id="c5a27-141">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Utbetalningsjournal** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c5a27-141">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c5a27-142">På sidan **Redigera betalningsjournal**, välj journalen **Bank**.</span><span class="sxs-lookup"><span data-stu-id="c5a27-142">On the **Edit Payment Journal** page, choose the **Bank** batch.</span></span>  
3. <span data-ttu-id="c5a27-143">Markera kryssrutan **Tillåt betalningsexport**.</span><span class="sxs-lookup"><span data-stu-id="c5a27-143">Choose the **Allow Payment Export** check box.</span></span>  

### <a name="to-specify-a-payment-method-for-a-vendor"></a><span data-ttu-id="c5a27-144">Ange betalningssätt för en leverantör</span><span class="sxs-lookup"><span data-stu-id="c5a27-144">To specify a payment method for a vendor</span></span>

<span data-ttu-id="c5a27-145">I följande tabell visas kombinationerna av betalningssätten FIK och GIRO som [!INCLUDE[prod_short](includes/prod_short.md)] stödjer.</span><span class="sxs-lookup"><span data-stu-id="c5a27-145">The following table shows the combinations of FIK and GIRO payment methods that [!INCLUDE[prod_short](includes/prod_short.md)] supports.</span></span>

|<span data-ttu-id="c5a27-146">Kombination</span><span class="sxs-lookup"><span data-stu-id="c5a27-146">Combination</span></span>|<span data-ttu-id="c5a27-147">Typ 01</span><span class="sxs-lookup"><span data-stu-id="c5a27-147">Type 01</span></span> | <span data-ttu-id="c5a27-148">Typ 04</span><span class="sxs-lookup"><span data-stu-id="c5a27-148">Type 04</span></span> | <span data-ttu-id="c5a27-149">Typ 71</span><span class="sxs-lookup"><span data-stu-id="c5a27-149">Type 71</span></span> | <span data-ttu-id="c5a27-150">Typ 73</span><span class="sxs-lookup"><span data-stu-id="c5a27-150">Type 73</span></span> |
|----|--------|---------|---------|---------|
|<span data-ttu-id="c5a27-151">Postgiro eller FIK fordringsägarenr?</span><span class="sxs-lookup"><span data-stu-id="c5a27-151">Giro Account No. or FIK Creditor No.?</span></span> | <span data-ttu-id="c5a27-152">Postgiro</span><span class="sxs-lookup"><span data-stu-id="c5a27-152">Giro Account No.</span></span> | <span data-ttu-id="c5a27-153">Postgiro</span><span class="sxs-lookup"><span data-stu-id="c5a27-153">Giro Account No.</span></span> | <span data-ttu-id="c5a27-154">FIK Fordringsägarenr.</span><span class="sxs-lookup"><span data-stu-id="c5a27-154">FIK Creditor No.</span></span> | <span data-ttu-id="c5a27-155">FIK Fordringsägarenr.</span><span class="sxs-lookup"><span data-stu-id="c5a27-155">FIK Creditor No.</span></span>|
|<span data-ttu-id="c5a27-156">Tillåta meddelande till mottagare?</span><span class="sxs-lookup"><span data-stu-id="c5a27-156">Allows Message to Recipient?</span></span> | <span data-ttu-id="c5a27-157">Ja</span><span class="sxs-lookup"><span data-stu-id="c5a27-157">Yes</span></span> |<span data-ttu-id="c5a27-158">Nej</span><span class="sxs-lookup"><span data-stu-id="c5a27-158">No</span></span> |<span data-ttu-id="c5a27-159">Nej</span><span class="sxs-lookup"><span data-stu-id="c5a27-159">No</span></span> | <span data-ttu-id="c5a27-160">Ja</span><span class="sxs-lookup"><span data-stu-id="c5a27-160">Yes</span></span> |
|<span data-ttu-id="c5a27-161">Innehåller betalningsreferensnummer?</span><span class="sxs-lookup"><span data-stu-id="c5a27-161">Contains Payment Reference number?</span></span> | <span data-ttu-id="c5a27-162">Nr</span><span class="sxs-lookup"><span data-stu-id="c5a27-162">No</span></span> | <span data-ttu-id="c5a27-163">Ja, 16 siffror.</span><span class="sxs-lookup"><span data-stu-id="c5a27-163">Yes, 16 digits.</span></span> | <span data-ttu-id="c5a27-164">Ja, 15 siffror.</span><span class="sxs-lookup"><span data-stu-id="c5a27-164">Yes, 15 digits.</span></span> | <span data-ttu-id="c5a27-165">Nej</span><span class="sxs-lookup"><span data-stu-id="c5a27-165">No</span></span>|

1. <span data-ttu-id="c5a27-166">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Leverantör** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c5a27-166">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c5a27-167">Öppna kortet, expandera fliken **betalningar** i fältet **betalningssätt** och välj betalningssätt.</span><span class="sxs-lookup"><span data-stu-id="c5a27-167">Open the card, expand the **Payments** tab, in the **Payment Method** field choose the payment method.</span></span>  
3. <span data-ttu-id="c5a27-168">I vissa fall måste du fylla i andra fält.</span><span class="sxs-lookup"><span data-stu-id="c5a27-168">Depending on your selection, you must complete other fields.</span></span> <span data-ttu-id="c5a27-169">Se tabellen ovan för mer information om kombinationer.</span><span class="sxs-lookup"><span data-stu-id="c5a27-169">See the table above for a description of the combinations.</span></span>  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a><span data-ttu-id="c5a27-170">Ange formaten som ska användas för ett bankkonto</span><span class="sxs-lookup"><span data-stu-id="c5a27-170">To specify the format to use for a bank account</span></span>

1. <span data-ttu-id="c5a27-171">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bankkonton** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c5a27-171">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c5a27-172">Öppna kortet för bankkontokort.</span><span class="sxs-lookup"><span data-stu-id="c5a27-172">Open the card for the bank account.</span></span>  
3. <span data-ttu-id="c5a27-173">I fältet **Format för betalningsexport**, välj format för exportfilen.</span><span class="sxs-lookup"><span data-stu-id="c5a27-173">In the **Payment Export Format** field, choose the format for your export file.</span></span>  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a><span data-ttu-id="c5a27-174">Välja FIK eller Giro betalningsinformation för leverantörsfakturor</span><span class="sxs-lookup"><span data-stu-id="c5a27-174">Choosing the FIK or Giro payment information for vendor invoices</span></span>

1. <span data-ttu-id="c5a27-175">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inköpsfakturor** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c5a27-175">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="c5a27-176">Välj Leverantören.</span><span class="sxs-lookup"><span data-stu-id="c5a27-176">Choose the vendor.</span></span> <span data-ttu-id="c5a27-177">Kom ihåg att detta måste en dansk leverantör med adress i Danmark.</span><span class="sxs-lookup"><span data-stu-id="c5a27-177">Remember, this must be a Danish vendor with an address in Denmark.</span></span>
3. <span data-ttu-id="c5a27-178">Skapa en faktura.</span><span class="sxs-lookup"><span data-stu-id="c5a27-178">Create an invoice.</span></span> <span data-ttu-id="c5a27-179">Fälten **betalningssätt** och **leverantörsnummer** fylls i baserat på inställningarna på leverantörskortet.</span><span class="sxs-lookup"><span data-stu-id="c5a27-179">The **Payment Method** and **Vendor Number** fields are filled in based on settings on the Vendor card.</span></span> <span data-ttu-id="c5a27-180">Du kan ändra dem om du vill.</span><span class="sxs-lookup"><span data-stu-id="c5a27-180">You can change them if you want.</span></span>
4. <span data-ttu-id="c5a27-181">I fältet **betalningsreferens** anger du det 15-siffriga numret på leverantörens faktura.</span><span class="sxs-lookup"><span data-stu-id="c5a27-181">In the **Payment Reference** field, enter the 15-digit number from the vendor invoice.</span></span>  

    > [!Tip]
    > <span data-ttu-id="c5a27-182">Du behöver bara lägga till de senaste 11 siffrorna.</span><span class="sxs-lookup"><span data-stu-id="c5a27-182">You only have to add the last 11 digits of the number.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="c5a27-183">lägger till fyra nollor i början av numret.</span><span class="sxs-lookup"><span data-stu-id="c5a27-183">will add four zeros to the beginning of the number.</span></span>  

5. <span data-ttu-id="c5a27-184">Bokföra fakturan</span><span class="sxs-lookup"><span data-stu-id="c5a27-184">Post the invoice.</span></span>

## <a name="to-use-the-extension-to-export-payment-data"></a><span data-ttu-id="c5a27-185">Du använder tillägget för att exportera betalningsdata</span><span class="sxs-lookup"><span data-stu-id="c5a27-185">To use the extension to export payment data</span></span>

1. <span data-ttu-id="c5a27-186">Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Utbetalningsjournaler** och välj sedan relaterad länk.</span><span class="sxs-lookup"><span data-stu-id="c5a27-186">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c5a27-187">Välj åtgärden **Föreslå betalningsjournaler för leverantör**.</span><span class="sxs-lookup"><span data-stu-id="c5a27-187">Choose the **Suggest Vendor Payment Journals** action.</span></span>  

    > [!Tip]
    > <span data-ttu-id="c5a27-188">Om du endast vill exportera specifika betalningar kan du använda alternativen för filtrering av data.</span><span class="sxs-lookup"><span data-stu-id="c5a27-188">If you want to export only specific payments, use the options for filtering the data.</span></span>  

3. <span data-ttu-id="c5a27-189">Om det behövs kan du lägga till filter om du endast vill exportera specifika betalningar.</span><span class="sxs-lookup"><span data-stu-id="c5a27-189">If needed, you can add filters to export only specific payments.</span></span>  
4. <span data-ttu-id="c5a27-190">I fältet **Bankbetalningstyp** väljer du **Elektronisk betalning.**</span><span class="sxs-lookup"><span data-stu-id="c5a27-190">In the **Bank Payment Type** field, choose **Electronic Payment**.</span></span>  
5. <span data-ttu-id="c5a27-191">Välj åtgärden **Exportera**.</span><span class="sxs-lookup"><span data-stu-id="c5a27-191">Choose the **Export** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c5a27-192">Se även</span><span class="sxs-lookup"><span data-stu-id="c5a27-192">See also</span></span>

<span data-ttu-id="c5a27-193">[Anpassning av Business Central för [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="c5a27-193">[Customizing Business Central for [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="c5a27-194">Samla in betalningar med SEPA-autogiro</span><span class="sxs-lookup"><span data-stu-id="c5a27-194">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="c5a27-195">Arbeta med redovisningsjournaler</span><span class="sxs-lookup"><span data-stu-id="c5a27-195">Working with General Journals</span></span>](ui-work-general-journals.md)  
